# Marstek Jupiter C Plus

Documentation and resources for the Marstek Jupiter C Plus.

## Known Issues

### Extension Battery Not Recognized

Press and hold the power button. When the light turns off, keep holding until the switch blinks, then release the button immediately.

### Error Code 0425

Overvoltage warning. Contact support for firmware update.

### Won't Charge/Discharge

This may be caused by a mismatch between firmware component versions. Contact support for firmware update.

## Modbus Communication

The device supports data reading via the **RS485 interface** using Modbus RTU protocol.

### RS485 Pinout

| Pin | Signal |
| --- | ------ |
| 1   | A      |
| 2   | B      |
| 3   | +5V    |
| 4   | -      |
| 5   | Ground |

**Note:** Pin 3 (+5V) does not appear to be working.

### Protocol & Serial Settings

- **Protocol:** Modbus RTU
- **Baud Rate:** 115200 bps
- **Data Bits:** 8
- **Stop Bits:** 1
- **Parity:** None
- **Flow Control:** None

### Read Holding Registers

| Register | Name                               | Bytes | Type | Gain/Unit | Read Value | Meaning | Description                                                                                                                  |
| -------- | ---------------------------------- | ----- | ---- | --------- | ---------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| 0x0001   | PV1 voltage                        | 2     | u16  | 0.1V      | 450(DEC)   | 45V     |                                                                                                                              |
| 0x0002   | PV1 current                        | 2     | u16  | 0.1A      | 150(DEC)   | 15A     |                                                                                                                              |
| 0x0003   | PV1 power                          | 2     | u16  | 1W        | 250(DEC)   | 250W    |                                                                                                                              |
| 0x0004   | PV2 voltage                        | 2     | u16  | 0.1V      | 450(DEC)   | 45V     |                                                                                                                              |
| 0x0005   | PV2 current                        | 2     | u16  | 0.1A      | 150(DEC)   | 15A     |                                                                                                                              |
| 0x0006   | PV2 power                          | 2     | u16  | 1W        | 250(DEC)   | 250W    |                                                                                                                              |
| 0x0007   | PV3 voltage                        | 2     | u16  | 0.1V      | 450(DEC)   | 45V     |                                                                                                                              |
| 0x0008   | PV3 current                        | 2     | u16  | 0.1A      | 150(DEC)   | 15A     |                                                                                                                              |
| 0x0009   | PV3 power                          | 2     | u16  | 1W        | 250(DEC)   | 250W    |                                                                                                                              |
| 0x000A   | PV4 voltage                        | 2     | u16  | 0.1V      | 450(DEC)   | 45V     |                                                                                                                              |
| 0x000B   | PV4 current                        | 2     | u16  | 0.1A      | 150(DEC)   | 15A     |                                                                                                                              |
| 0x000C   | PV4 power                          | 2     | u16  | 1W        | 250(DEC)   | 250W    |                                                                                                                              |
| 0x000D   | Grid power                         | 2     | u16  | 1W        | 500(DEC)   | 500W    |                                                                                                                              |
| 0x000F   | Battery voltage                    | 2     | u16  | 0.1V      | 550(DEC)   | 55V     |                                                                                                                              |
| 0x0010   | Battery SOC                        | 2     | u16  | 1%        | 50(DEC)    | 50%     |                                                                                                                              |
| 0x0013   | Daily power generation             | 4     | u32  | 0.01kWh   | 100(DEC)   | 1kWh    |                                                                                                                              |
| 0x0015   | Monthly power generation           | 4     | u32  | 0.01kWh   | 100(DEC)   | 1kWh    |                                                                                                                              |
| 0x0017   | Daily grid-connected electricity   | 4     | u32  | 0.01kWh   | 100(DEC)   | 1kWh    |                                                                                                                              |
| 0x0019   | Monthly grid-connected electricity | 4     | u32  | 0.01kWh   | 100(DEC)   | 1kWh    |                                                                                                                              |
| 0x001B   | Device ID                          | 2     | u16  |           |            |         |                                                                                                                              |
| 0x001C   | EMS version                        | 2     | u16  |           |            |         |                                                                                                                              |
| 0x001D   | INV version                        | 2     | u16  |           |            |         |                                                                                                                              |
| 0x001E   | MPPT version                       | 2     | u16  |           |            |         |                                                                                                                              |
| 0x001F   | BMS version                        | 2     | u16  |           |            |         |                                                                                                                              |
| 0x0022   | Screen version                     | 2     | u16  |           |            |         |                                                                                                                              |
| 0x0025   | Device type                        | 2     | u16  |           |            |         | 0: jupiter-c-800W<br>1: jupiter-c-1000W<br>2: jupiter-c-600W<br>3: jupiter-e-800W<br>4: jupiter-e-1000W<br>5: jupiter-e-600W |
| 0x1004   | PV1 working status                 | 2     | u16  |           |            |         | 0: not working<br>1: working                                                                                                 |
| 0x1005   | PV2 working status                 | 2     | u16  |           |            |         | 0: not working<br>1: working                                                                                                 |
| 0x1006   | PV3 working status                 | 2     | u16  |           |            |         | 0: not working<br>1: working                                                                                                 |
| 0x1007   | PV4 working status                 | 2     | u16  |           |            |         | 0: not working<br>1: working                                                                                                 |
| 0x1008   | INV working status                 | 2     | u16  |           |            |         | 0: not working<br>1: working                                                                                                 |

## References

- [User Manual](marstek-jupiter-c-plus-user-manual.pdf)
- [Official Marstek Jupiter C Plus Website](https://marstekenergy.com/products/marstek-jupiter-c-plus-all-in-one)
