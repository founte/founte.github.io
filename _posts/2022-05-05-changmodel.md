# img Version: 0.6.5

## Release date: 2021/09/30

####  Artosyn SDK

* [**New**]增加logrotate日志控制
* [**New**]应用使用软件看门狗

# img Version: 0.6.4

## Release date: 2021/09/27

####  算法

* [**Fix**]修复CPU占用过高问题

# img Version: 0.6.3

## Release date: 2021/09/03

####  sdk v1.82.9

* [**Fix**] 修复close dev时候assert问题
* [**Fix**] 修复录像灰度图问题 

####  dmcamd

* [**Enhance**] 稳定性问题，修复可能存在的内存问题

####  算法

* [**New**]增加设置log保存路径和log等级的功能
* [**New**]实现贯通道设备上电持续录像，并每5s上报一次计数结果
* [**Fix**]SDK使用0831版本，修复读取oni灰度图异常问题
* [**Fix**]IP设置与拨码值对应关系不符合文档规定的问题

# img Version: 0.6.2

## Release date: 2021/08/18

####  dmcamd

* [**Enhance**] V1.2 硬件稳定性问题

####  **算法**

* [**Enhance**] 前端状态显示只有计数中和车门关闭两种状态
* [**New**] 更新UPL_RES包的解析

# img Version: 0.6.1

## Release date: 2021/08/17

####  Artosyn SDK

* [**Fix**]修复组播无法搜到设备问题

# img Version: 0.6

## Release date: 2021/08/16

#### dmcamd：2.3.2

* [**New**]支持DE/非DE自动识别切换

####  Artosyn SDK

* [**Fix**]批量升级问题修复

#### 算法

-  **dmhc_app** **1.0.3**
   - [**Fix**] 修复dmhc_app接受reload信号报错问题
   - [**New**] 增加ftp上传功能
   - [**New**]ntp校时，每5分钟一次，仅在算法核关闭时启动
-  **dmhc_app** **0.2.0**
   - [**New**]批量配置算法参数会永久生效
   - [**New**]算法关闭使能之后仍然可以更新图片
   - [**Fix**] 修正轨迹列表引起的性能问题
   - [**New**]实现保存录像功能，使用MPEG-4压缩
   - [**New**]算法核默认不使能，需要通过接口开启使能
   - [**New**]增加注册分类器处理函数的接口，可以自定义神经网络推理函数，默认使用opencv dnn
   - [**Fix**]修正粗提案点过多引起的性能问题
   - [**New**]将所有日志的保存路径改为/database/log/