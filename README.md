# Tesla Model 3 LFP Pack

Photos and diagnostic data from a Tesla Model 3 LFP (RWD) high-voltage battery pack, read over CAN using a LilyGo T-CAN485 running open BMS emulator firmware.

## Pack identification

| Field | Value |
| --- | --- |
| Battery Serial Number | TG322294004L47 |
| Battery Part Number | 1666968-99-C |
| PCS Part Number | 1135558-03-D |
| Style | 8U |
| Type | E14 |
| Assembly | HVBAT 400VDC |
| Phase / Platform | 1PH, M3 (Model 3) |
| Manufacture Date | 2022-10-21 |
| Origin | Made in China |
| Pack Mass | 502.00 kg |
| Rated Energy | 60.0 kWh |
| Rated Capacity | 172.5 Ah |
| Chemistry | LFP (prismatic) |

Photos of the physical labels are in [`photos/IMG_5924.JPG`](photos/IMG_5924.JPG), [`photos/IMG_5925.JPG`](photos/IMG_5925.JPG), and [`photos/IMG_5926.JPG`](photos/IMG_5926.JPG).

## Pack state at readout

| Field | Value |
| --- | --- |
| State of Charge (SOC) | 0.60% |
| State of Health (SOH) | 99.00% (calculated 103.33) |
| Pack Voltage | 309.8 V |
| Current | 0.0 A |
| Power | 0 W |
| Total Capacity | 62.0 kWh |
| Remaining Capacity | 372 Wh |
| Nominal Full Pack Energy | 62.00 kWh |
| Beginning-of-Life Energy | 60.00 kWh |
| Energy to Charge Complete | 49.22 kWh |
| Lifetime Discharge | 41,684.45 kWh |
| Lifetime Charge | 44,104.53 kWh |
| Battery State | Idle / STANDBY |
| System Status | FAULT (high-voltage cable disconnected during readout) |

## Cell-level data (108 cells)

| Field | Value |
| --- | --- |
| Cell Min Voltage | 2764 mV (Cell 17) |
| Cell Max Voltage | 2967 mV (Cell 1) |
| Cell Delta | 203–204 mV |
| Temp Min / Max | 28.0 °C / 40.5 °C |
| Brick Voltage Max / Min | 2.97 V / 2.76 V |
| Brick Temp Max / Min Index | 5 / 4 |

Per-cell voltage screenshots: [`IMG_5918.PNG`](photos/IMG_5918.PNG), [`IMG_5919.PNG`](photos/IMG_5919.PNG), [`IMG_5920.PNG`](photos/IMG_5920.PNG), [`IMG_5921.PNG`](photos/IMG_5921.PNG) (bar-chart view).

The low SOC (0.6%) explains the wide delta — LFP cells diverge noticeably at the bottom of the SOC curve. SOH is still effectively new.

## Contactor / HV state

| Field | Value |
| --- | --- |
| HVIL Status | UNKNOWN or CONTACTORS OPEN |
| HVP Contactor State | OPEN |
| BMS Contactor State | OPEN |
| Negative Contactor | OPEN |
| Positive Contactor | OPEN |
| Closing Blocked | No |
| Pyrotest in Progress | No |
| DC Link Allowed to Energize | Yes |
| HVP pack voltage | 309.60 V |
| HVP dcLink voltage | 9.60 V |
| HVP pack contactor coil current | 0.00 A |
| HVP 12V supply | 13.30 V |

## Thermal / PCS

| Field | Value |
| --- | --- |
| PCS dcdc Temp | 31.60 °C |
| PCS Ambient Temp | 33.90 °C |
| PCS Chg PhA / PhB / PhC | 34.10 / 30.40 / 31.40 °C |
| Pack Temp Min / Max | 26.00 / 40.50 °C |
| Inlet Active Cool Target | 46.00 °C |
| Inlet Passive Target | 30.00 °C |
| Inlet Active Heat Target | -7.50 °C |
| Flow Request | 0.00 LPM |

## Hardware / firmware

| Field | Value |
| --- | --- |
| Reader hardware | LilyGo T-CAN485 |
| Reader firmware | 10.8.0 |
| Web UI | `http://192.168.4.1/` |
| Battery protocol | Tesla Model 3/Y (LFP) |
| BMS buildConfigId / hardwareId / componentId | 8205 / 8 / 136 |
| HVP buildConfigId / hardwareId / componentId | 8205 / 8 / 135 |
| PCS buildConfigId / hardwareId / componentId | 8205 / 252 / 27 |

## Photo index

| File | Contents |
| --- | --- |
| [IMG_5908](photos/IMG_5908.PNG) | Main pack summary — SOC/SOH/voltage/temps, FAULT status |
| [IMG_5909](photos/IMG_5909.PNG) | Main pack summary (second view) |
| [IMG_5910](photos/IMG_5910.PNG) | Fault log — INTERNAL_OPEN_FAULT, CELL_UNDER_VOLTAGE, CAN_NATIVE_TX_FAILURE |
| [IMG_5911](photos/IMG_5911.PNG) | Pack identity — serial, part numbers, mass, contactor/HVIL state |
| [IMG_5912](photos/IMG_5912.PNG) | BMS detail — calculated SOH, nominal energies, isolation, build IDs |
| [IMG_5913](photos/IMG_5913.PNG) | PCS detail — brick V/T, PCS temps, power limits, flow targets |
| [IMG_5914](photos/IMG_5914.PNG) | PCS state machine — standby, precharge, build IDs |
| [IMG_5915](photos/IMG_5915.PNG) | PCS dcdc internals + HVP block |
| [IMG_5916](photos/IMG_5916.PNG) | HVP detail — pack/contactor voltages, GPIO states |
| [IMG_5917](photos/IMG_5917.PNG) | HVP GPIOs and shunt/aux current sense |
| [IMG_5918](photos/IMG_5918.PNG) | Per-cell voltages — cells 1–44 |
| [IMG_5919](photos/IMG_5919.PNG) | Per-cell voltages — cells 25–76 |
| [IMG_5920](photos/IMG_5920.PNG) | Per-cell voltages — cells 53–104 |
| [IMG_5921](photos/IMG_5921.PNG) | Per-cell voltages — cells 81–108 + bar chart |
| [IMG_5922](photos/IMG_5922.PNG) | Main summary, later reading (temp 41.0 °C) |
| [IMG_5923](photos/IMG_5923.PNG) | Fault log — cumulative cell undervoltage count grew to 237 |
| [IMG_5924](photos/IMG_5924.JPG) | Physical label "8U" on pack housing |
| [IMG_5925](photos/IMG_5925.JPG) | Chinese-market rating label — 60.0 kWh / 172.5 Ah |
| [IMG_5926](photos/IMG_5926.JPG) | Tesla part-number label with QR code |
