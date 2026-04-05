# 1. Feature Overview

This USRP B210 is an optimized improvement over the original design, using the newer K7 series FPGA in place of the original S6 series. It supports Vivado development and maintains compatibility with original functionality. Key similarities and differences from the original are as follows:

- Uses a USB 3.0 Type-C interface, with a maximum real-time transfer bandwidth of 56 MHz
- The RF front-end is consistent with the original, using a band-segmented design with RF circuitry optimized through simulation
- Supports PPS and 10 MHz reference input; adds an onboard GPS module that can substitute for the PPS input
- The GPSDO slot has been removed to reduce board size; overall dimensions are 70 × 97 × 11.5 mm

# 2. Usage Notes

Differences from the original in operation:

- Before use, the `usrp_b210_fpga.bin` file on the host computer must be replaced
- The GPSDO module cannot be connected
- The GPS module's PPS signal takes priority over external PPS; when the GPS module has a lock, the external PPS input is unavailable

# 3. Interface Reference

| Label | Description |
|-------|-------------|
| GPS | Antenna input for the GPS module — MMCX connector |
| USB | USB 3.0 data communication with the host — Type-C connector |
| PPS | External PPS input — MMCX connector |
| 10M | 10 MHz reference input — MMCX connector |
| TRX1 | Transmit/receive port 1 — SMA connector |
| RX1 | Receive-only port 1 — SMA connector |
| RX2 | Receive-only port 2 — SMA connector |
| TRX2 | Transmit/receive port 2 — SMA connector |
| FPC Connector | JTAG debug port and extended GPIO |
| PWER LED | Power indicator LED — red when powered on |
| STAS LED | Status indicator LED — blue after firmware is loaded |
| CLK LED | PPS indicator LED — flashes red in sync with the currently selected PPS pulse |
| USR LED | No function assigned; user-configurable |
| TRX1 LED | Transmit/receive indicator LED — red during transmit, blue during receive |
| RX1 LED | Receive indicator LED — blue during receive |
| RX2 LED | Receive indicator LED — blue during receive |
| TRX2 LED | Transmit/receive indicator LED — red during transmit, blue during receive |
