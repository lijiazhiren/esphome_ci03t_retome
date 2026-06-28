ci03t本身也可以作为一个遥控器使用

在官方平台有通用的空调遥控代码 

设置好以后 喊出 匹配空调 就会进入匹配模式  

这时说出你的空调品牌就能自动匹配了

能匹配大多数品牌

但是只测试过一个格力空调

因为esphome空调组件没有模板类型的

因此设置了一个esphome的遥控空调来作为前端使用 

设置的遥控组件是必须的  

方案思路为  

使用语音直接让ci03t的红外遥控空调 同时ci03t通过串口把遥控的命令同步给esphome的空调组件


也可以让esphome的空调组件通过串口发送命令让ci03t遥控空调

这两个功能是双向的  

ci03t的红外电路是必须的  esphome的可以自由设置

使用方法 
https://www.smartpi.cn
在ci03t官网上传 CI-03T 20260629003.json 生成固件下载刷入
本配置设置的引脚
ci03t_pb5---->>esp_rx
ci03t_pb6<<----esp_tx

pa0===IR_TX(红外电路的输入引脚)

ci03t设置的命令词

match_air=匹配空调@好的、开始匹配

open_air=打开空调@好的、启动空调

close_air=关闭空调@好的、空调关闭

air_16=十六度@空调十六度

air_17=十七度@空调十七度

air_18=十八度@空调十八度

air_19=十九度@空调十九度

air_20=二十度@空调二十度

air_21=二十一度@空调二十一度

air_22=二十二度@空调二十二度

air_23=二十三度@空调二十三度

air_24=二十四度@空调二十四度

air_25=二十五度@空调二十五度

air_26=二十六度@空调二十六度

air_27=二十七度@空调二十七度

air_28=二十八度@空调二十八度

air_29=二十九度@空调二十九度

air_30=三十度@空调三十度

air_mode_cold=制冷模式@空调制冷模式

air_node_hot=制热模式@空调制热模式

air_mode_supply=送风模式@空调送风模式

air_fan_mid=空调中速风@空调二档风

air_fan_low=空调低速风@空调一档风

air_swing=上下扫风@打开上下扫风

air_swingh=左右扫风@打开左右扫风

air_swing_off=停止上下扫风@空调停止上下扫风

air_swingh_off=停止左右扫风@空调停止左右扫风

air_temp_up=升高温度@空调温度增加

air_temp_down=降低温度@空调温度减小

air_fan_sp_up=增加风速@好的、风速加大

air_fan_sp_down=减小风速@空调风速减小

air_auxheat_off=关闭电加热@空调关闭电加热

air_led_close=关闭数显@空调关闭数显

air_led_open=打开数显@空调打开数显

air_mode_dry=除湿模式@空调除湿模式

air_fan_auto=自动风速@空调自动风速

air_fan_high=空调高速风@空调三档风

air_mode_auto=空调自动模式@空调冷暖模式

airpreset_sleep=空调睡眠模式@好的

air_stop_sleep=空调关闭睡眠模式@好的

air_swing_allon=开启扫风@空调打开扫风

airswing_alloff=停止扫风@空调停止扫风

``




