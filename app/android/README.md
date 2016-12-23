Android SDK


 
/*******************************

功能描述：XAI构造器详细资料
参数1：云服务器地址
参数2：云服务器TCP端口
参数3：消息回调接口

*********************************/

public XAI(java.lang.String host,int port,XAICallback c0)

/*******************************

功能描述：建立网络连接（登录）
参数1：登录名（设备编号）
参数2：登录密码
返回值：ERRNO

*********************************/

public ERRNO start(long luid,java.lang.String pwd,java.lang.String ca_file,java.lang.String dir_persistence)

/*******************************

功能描述：建立网络连接（登录）
参数1：所属网关编号
参数2：登录名
参数3：登录密码
返回值：ERRNO

*********************************/

public ERRNO start(int apsn, long luid, String pwd, String ca_file, String dir_persistence)

/*******************************

功能描述：链接注销

*********************************/

public void close()


/*******************************

功能描述：发送本机设备信息
参数1：设备类型
参数2：软件版本
返回值：ERRNO

*********************************/

public ERRNO sendMyDev(int type, int ver, boolean will_sleep)

/*******************************

功能描述：发送本机设备信息
参数1：是否在线
返回值：ERRNO

*********************************/

public ERRNO sendMyDeviceConnection(boolean online)

/*******************************

功能描述：发送本机名字
参数1：名字
返回值：ERRNO

*********************************/

public ERRNO sendMyDeviceName(java.lang.String name)

/*******************************

功能描述：发送本机设备电量信息
参数1：电量（0-100）
返回值：ERRNO

*********************************/

public ERRNO sendMyDevicePower(int power)

/*******************************

功能描述：发送自己设备的状态信息
参数1：状态编号
参数2：数据类型
参数3：数据
返回值：ERRNO

*********************************/

public ERRNO sendStatus(int id,int data_type,byte[] data)

/*******************************

功能描述：发送控制命令到指定用户、设备
参数1：指定用户所属的网关编号
参数2：指定用户、设备的设备编号
参数3：控制命令编号
参数4：数据类型
参数5：数据
返回值：ERRNO

*********************************/

public ERRNO sendCmd(int apsn,long luid,int id,int data_type,byte[] data)

/*******************************

功能描述：发送聊天消息到指定用户、设备
参数1：指定用户所属的网关编号
参数2：指定用户、设备的设备编号
参数3：数据类型
参数4：数据
返回值：ERRNO

*********************************/

public ERRNO sendIM(int apsn,long luid,int data_type,byte[] data)

/*******************************

功能描述：添加设备到指定网关
参数1：设备所属网关
参数2：设备编号
返回值：ERRNO

*********************************/

public ERRNO deviceAdd(int apsn,long luid)

/*******************************

功能描述：从指定网关删除设备
参数1：设备所属网关
参数2：设备编号
返回值：ERRNO

*********************************/

public ERRNO deviceRemove(int apsn,long luid)

/*******************************

功能描述：注册手机用户
参数1：用户手机设备编号
参数2：用户密码
返回值：ERRNO

*********************************/

public ERRNO userRegister(long luid,java.lang.String pwd)

/*******************************

功能描述：删除手机用户
参数1：用户手机设备编号
参数2：用户密码
返回值：ERRNO

*********************************/

public ERRNO userRemove(long luid,java.lang.String pwd)

/*******************************

功能描述：重置用户密码
参数1：用户手机设备编号
参数2：用户密码
返回值：ERRNO

*********************************/

public ERRNO pwdReset(long luid,java.lang.String pwd)

/*******************************

功能描述：修改用户密码
参数1：用户手机设备编号
参数2：旧密码
参数3：新密码
返回值：ERRNO

*********************************/

public ERRNO pwdChange(long luid,java.lang.String pwd_old,java.lang.String pwd_new)

/*******************************

功能描述：添加联动到指定网关
参数1：待添加到的网关编号
参数2：联动条件组
参数3：联动动作组
返回值：ERRNO

*********************************/

public ERRNO linkAdd(int apsn,java.lang.String name,java.util.ArrayList<LINK_ITEM_DES> condition,java.util.ArrayList<LINK_ITEM_DES> action)

/*******************************

功能描述：设置指定网关上的联动状态
参数1：联动所在的网关编号
参数2：联动编号
参数3：启用还是禁用
返回值：ERRNO

*********************************/

public ERRNO linkSet(int apsn,int id,boolean active)

/*******************************

功能描述：删除指定网关上的联动
参数1：联动所在的网关编号
参数2：联动编号
返回值：ERRNO

*********************************/

public ERRNO linkRemove(int apsn,int id)

/*******************************

功能描述：运行指定网关上的联动
参数1：联动所在的网关编号
参数2：联动编号
返回值：ERRNO

*********************************/

public ERRNO linkRun(int apsn,int id)

/*******************************

功能描述：设置网关是否开启白名单模式
参数1：要设置白名单模式的网关编号
参数2：是否开启白名单
返回值：ERRNO

*********************************/

public ERRNO setWhiteListEnable(int apsn,boolean enable)

/*******************************

功能描述：设置推送标记
参数1：推送标志所属网关
参数2：JPUSH注册ID
参数3：是否开启推送
参数4：推送配置数据
返回值：ERRNO

*********************************/

public ERRNO setJPushConfig(int apsn,java.lang.String registerID,boolean enable,java.util.ArrayList<JPUSH_CONFIG> configs)

/*******************************

功能描述：检查网络延迟
返回值：网络延迟，单位ms

*********************************/

public int detectNetworkDelay_MS()

/*******************************

功能描述：通过手机号生成手机设备的编号
参数1：手机号
返回值：手机设备编号

*********************************/

public static long mobileToLuid(java.lang.String mobile)

/*******************************

功能描述：将手机设备编号转换为手机号
参数1：手机设备编号
返回值：手机号

*********************************/

public static java.lang.String luidToMobile(long luid)

/*******************************

功能描述：服务器是否已连接
返回值：连接状态

*********************************/

public boolean isConnected()

/*******************************

功能描述：将当前登录手机号绑定到指定网关
参数1： 待绑定的网关编号
返回值：ERRNO

*********************************/

public ERRNO gatewayBind(int apsn)

/*******************************

功能描述：解除当前登录手机号对网关的绑定
参数1： 要解除绑定的网关编号
返回值：ERRNO

*********************************/

public ERRNO gatewayUnbind(int apsn)

/*******************************

功能描述：在局域网搜索所有网关
参数1： 搜索时长
返回值：网关列表

*********************************/

public static java.util.ArrayList<java.lang.String> gatewayLocalSearch(int timewait_ms)

/*******************************

功能描述：在局域网绑定网关
参数1： 绑定者的LUID
参数2：网关列表

*********************************/

public static int gatewayLocalBind(long luid_mobile,java.util.ArrayList<java.lang.String> gateway_list)

/*******************************

功能描述：在局域网绑定网关
参数1： 绑定者的LUID
参数2：网关IP地址
参数1： 网关编号
参数2：设置的网关名字
返回值：true: 成功, false:失败

*********************************/

public static boolean gatewayLocalBind(long luid_mobile,java.lang.String gateway_ip,int apsn_gateway,java.lang.String name)





public enum ERRNOextends java.lang.Enum<ERRNO>

ARG_INCORRECT
13:参数错误

CONNECTON_LOST
139:连接丢失

DEVICE_NONE_EXISTED
11:设备不存在

DEVICE_OFFLINE
12:设备离线

FIRMWARE_NOT_LATEST
34:有新固件

GENERAL_ERROR
2:通用错误

IP_FAILED
136:IP不正确

LINK_EXISTED
29:联动已存在

LINK_NOT_EXISTED
30:联动不存在

LINK_WILL_DEACTIVE
35:联动即将失效

LOW_POWER
14:电量低

LUID_EXISTED
7:设备编号已存

LUID_INVALID
8:在设备编号无效

LUID_NOT_EXISTED
9:设备编号不存在

MALLOC_ERROR
15:内存不足

NAME_EXISTED
4:用户名已存在

NAME_INVALID
5:用户名无效

NAME_NONE_EXISTED
6:户不存在

NEED_RETRY
32:需要重试

NETWORK_FAILED
137:网络错误

NO_PRIV
3:无权限

OK
0:正常

OTA_FINISHED
36:OTA升级完成

OTA_NEXT
37:OTA请求下一个数据块

PWD_INCORRECT
10:密码错误

PWD_INVALID
28:密码不正确

TIMEOUT
16:内存不足

TOKEN_INCORRECT
33:TOKEN不正确

TOKEN_NOT_EXIST
31:TOKEN不存在

UNCHANGE
1 :操作没有导致任何变化

