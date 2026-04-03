> [!NOTE]  
> Welcome! The `usrp_b210_fpga.bin` is located [here](/需替换BIN文件/usrp_b210_fpga.bin) (you must replace it in your UHD images folder).<br>All documentation in this repository is in Chinese, as it was received this way and has been kept unmodified.

This software was received with the **Upgraded USRP B210 AD9361BBCZ + XC7K325T** clone from HamGeek.

# 1. 功能说明

此 USRP B210 基于原版优化改进而来，使用较新系列的 K7 替代原版的 S6 系列，支持
Vivado 开发，兼容原版功能。与原版的主要异同点如下：

- 采用 USB3.0 Type-C 接口，最大实时传输带宽可达 56MHZ；
- 射频前端与原版一致，采用分频段设计，射频线路经过仿真优化；
- 支持 PPS、10MHZ 输入，添加板载 GPS 模块，可替代 PPS 输入；
- 移除 GPSDO 插槽，缩小板卡尺寸，整体体积为 70*97*11.5mm

# 2. 使用说明

与原版使用上的差异：

- 使用前需替换电脑内 usrp_b210_fpga.bin 文件；
- 不可接入 GPSDO 模块；
- GPS 模块的 PPS 优先级高于外部 PPS，当 GPS 模块锁定时，外部 PPS 输入不可用；

# 3. 接口说明

| 标识 | 说明 |
|------|------|
| GPS | GPS 模块的天线输入，MMCX 接口 |
| USB | USB3.0 与主机数据通信，Type-C 接口 |
| PPS | 外部 PPS 输入，MMCX 接口 |
| 10M | 10M 参考输入，MMCX 接口 |
| TRX1 | 发射或接收端口 1，SMA 接口 |
| RX1 | 接收端口 1，SMA 接口 |
| RX2 | 接收端口 2，SMA 接口 |
| TRX2 | 发射或接收端口 2，SMA 接口 |
| FPC 连接器 | JTAG 调试口及外扩 GPIO |
| PWER LED | 电源指示 LED，通电后即为红色 |
| STAS LED | 状态指示 LED，加载固件后为蓝色 |
| CLK LED | PPS 指示 LED，红色闪烁与当前选择的 PPS 脉冲同步 |
| USR LED | 暂无功能，可自定义 |
| TRX1 LED | 发射接收指示 LED，发射时为红色，接收时为蓝色 |
| RX1 LED | 接收指示 LED，接收时为蓝色 |
| RX2 LED | 接收指示 LED，接收时为蓝色 |
| TRX2 LED | 发射接收指示 LED，发射时为红色，接收时为蓝色 |
