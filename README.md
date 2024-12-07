# 云快充协议+云快充1.5协议+云快充1.6+云快充协议开源代码+云快充底层协议+云快充桩直连+桩直连协议+充电桩协议+云快充源码

# 一、介绍

云快充协议+云快充1.5协议+云快充1.6+云快充协议开源代码+云快充底层协议+云快充桩直连+桩直连协议+充电桩协议+云快充源码

# 二、软件架构

1、提供云快充底层桩直连协议，版本为云快充1.5，对于没有对接过充电桩系统的开发者尤为合适；

2、包含：启动充电、结束充电、充电中实时数据获取、报文解析、Netty通讯框架、包解析工具、调试器模拟器软件等；

# 三、功能清单

SpringBoot框架+Netty通讯服务+云快充1.4-1.5-1.6协议模块介绍

开发语言：Java 框架：SpringBoot 部署：独立的项目、独立运行、独立部署，也可集成到自己的充电平台

充电桩支持：公牛、盛宏、特来电、小桔、云快充、万马、驴充充、南瑞、京能、星星、双杰、普天等，只要桩支持刷云快充协议，均可对接；

# 四、接口说明

1、netty的channel仓储 2、频道绑定 key 3、客户端和频道绑定 4、存储频道 5、重入锁 6、获取单机连接数量 7、绑定频道和客户端id 8、是否已连接 9、是否已登录 10、获取客户端id 11、获取频道 12、释放连接和资源 13、关闭和清理连接 14、给设备发消息 15、Channel基础类 16、读取SIM卡号 0x76 17、 远程重启 0x92* 重启充电桩，应对部分问题，如卡死等 18、 * 远程更新 0x94 * 对桩进行软件升级，平台升级模式为ftp文件升级，由桩企提供升级需要的更新文件（文件名由桩企定义）* 平台再数据帧中提供访问更新文件相关服务器地址及下载路径信息，桩下载完更新程序后对文件进行校验并进行升级。 19、位数不够，进行补零操作 20、桩启动处理 21、离线充电-创建离线订单的订单号 22、结束订单 23、保存订单结算数据 24、* 更新设备停止状态 * 0X35 远程停机命令 25、充电过程数据存储 26、计算服务费 27、实时监测数据处理 28、保存错误日志 29、充电桩状态获取：0离线 1空闲-未插枪 2空闲-已插枪 3充电中 4已充满 5故障 6就绪 30、 获取log key 31、计算充电电费 32、组装报文的开始信息 33、编写帧校验位并重置指针位置 34、获取报序号 35、保存消息日志 36、处理数据 37、获取设备错误代码 38、处理netty的数据 39、发送获取实时数据命令0x12 40、远程账户余额更新 0x42 平台在用户完成充值后会将用户更新的余额下发到充电桩,* 桩接收到此数据帧需要对当前充电用户的信息进行校验并更新余额信息 41、 离线卡数据清除 0x46 * 平台再充电桩在线时下发此数据帧，充电桩接收到报文后清除桩本地对应的离线卡数据 42、离线卡数据查询 0x48 * 平台再充电桩在线时下发此数据帧到充电桩，充电桩接收到该报文后查询桩本地是否存在对应的离线卡 43、工作参数设置 0x52 采用云快充1.8版本 * 远程设置充电桩是否停用；设置充电桩允许输出功率，以实现电网功率的调节 44、对时设置 0x56 * 运营平台同步充电桩时钟，以确保充电桩与运营平台的时钟一致 45、 计费模型设置 0x58 * 用户充电费用计算，每半小时为一个费率段，共48段， * 每段对应尖峰平谷其中一个费率充电时桩屏幕按此费率分别显示已充电费和服务费 46、读取SIM卡号 0x76 47、远程重启 0x92 48、ota升级 49、启动充电 50、结束充电 51、设备启停测试用

# 五、常用聚合接口： 

1、netty处理服务 2、发送获取实时数据命令0x12 3、远程账户余额更新 0x42 4、离线卡数据清除 0x46 5、离线卡数据查询 0x48 6、获取或者清除离线卡数据 7、工作参数设置 0x52 8、对时设置 0x56 9、计费模型设置 0x58 10、OTA升级 11、启动充电 12、结束充电

# 六、源码合作

提供完整云快充协议源代码，自己可以对接充电桩进行测试和调试；

# 七、界面展示

![extending-a-theme](/001.png)
![extending-a-theme](/002.png)
![extending-a-theme](/003.jpg)
![extending-a-theme](/004.png)
![extending-a-theme](/005.jpg)
![extending-a-theme](/lianxi.jpg)

