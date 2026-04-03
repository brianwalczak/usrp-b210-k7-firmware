## 1. 功能说明

## 此USRPB 210 基于原版优化改进而来，使用较新系列的K 7 替代原版的S 6 系列，支持

Vivado开发，兼容原版功能。与原版的主要异同点如下：
 采用USB 3. 0 Type-C接口，最大实时传输带宽可达 56 MHZ；
 射频前端与原版一致，采用分频段设计，射频线路经过仿真优化；
 支持PPS、 10 MHZ输入，添加板载GPS模块，可替代PPS输入；
 移除GPSDO插槽，缩小板卡尺寸，整体体积为 70 * 97 * 11. 5 mm

2. 使用说明
与原版使用上的差异：
 使用前需替换电脑内usrp_b 210 _fpga.bin文件；
 不可接入GPSDO模块；
 GPS模块的PPS优先级高于外部PPS，当GPS模块锁定时，外部PPS输入不可用；

3. 接口说明
GPS GPS模块的天线输入，MMCX接口
USB USB 3. 0 与主机数据通信，Type-C接口
PPS 外部PPS输入，MMCX接口
10 M 10 M参考输入，MMCX接口

TRX (^1) 发射或接收端口 1 ，SMA接口
RX 1 接收端口 1 ，SMA接口
RX 2 接收端口 2 ，SMA接口
TRX 2 发射或接收端口 2 ，SMA接口
FPC连接器 JTAG调试口及外扩GPIO
PWERLED 电源指示LED，通电后即为红色
STASLED 状态指示LED，加载固件后为蓝色
CLKLED PPS指示LED，红色闪烁与当前选择的PPS脉冲同步
USRLED 暂无功能，可自定义
TRX 1 LED 发射接收指示LED，发射时为红色，接收时为蓝色
RX 1 LED 接收指示LED，接收时为蓝色
RX 2 LED 接收指示LED，接收时为蓝色
TRX 2 LED 发射接收指示LED，发射时为红色，接收时为蓝色


