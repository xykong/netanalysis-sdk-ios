# UNetAnalysisSDK release history 

## v1.0

###  v-1.0.1(2019.01.29)

* 设置SDK的日志级别(推荐：在研发调试时设置为`DEBUG`级别，在发布时设置为`ERROR`级别)
* 支持用户设置`app`主服务`IP`地址，用于网络诊断
* 支持自动网络诊断并上报
* 支持手动网络诊断并上报
* 支持获取SDK版本号

###  v-1.0.2(2019.01.30)

* 修复bug：苹果reachibality冲突

### v-1.0.5(2019.02.22)

* 更新上报数据字段
* 更新手动诊断逻辑
* 当app进入非活跃状态时，停止网络数据收集

### v-1.0.7

* 更新数据上报逻辑
* 更新http超时时间为60s

### v-1.0.11(2019.03.08)

* 修复bug: 因线程挂起导致ping的结果不准确
* 修复bug: 丢掉无效上报数据

### v-1.0.12(2019.07.01)

* 修复bug: tracert到达目的主机时，校验的icmp包的类型应该是replay包，而不是timeout包
* 添加uuid字段(删除应用重装app会变化)
* 支持用户自定义字段接
* 添加ping校验：当ping一个主机时，如果完全丢包，则判断一下当前终端是否被禁ping了，由此可提高最终统计loss100%的精确性
* 对于u host不做tracert

### v-1.0.13(2019.07.11)

* 移除手动诊断接口


## v2.0

### v2.0.1(2019.08.13)

* 新增功能： 
	* 支持关闭自动检测网络逻辑，可以自己手动触发网络检测
	* 为上报的网络数据增加数据来源类型(自动检测触发、手动检测触发)
	* SDK内部增加线上开关
* bug修复：
	* 在ios12上`URLSession data request is cancelled as soon as app is not in foreground with error code 53`导致cpu占用过高
	* 修复了部分内存泄漏问题
	* 修复了其它一些bug

### v2.0.2(2019.09.23)

* bug修复 
* 适配ios13 