# Function

- Obniz monitors CO2 level periodically (TBD: every miniutes)
- CO2 level is shown on obniz display
- Above 1500ppm LED light alerts.

TBD ###  at this point, browser required to run obniz.  Later server will run obniz thru API.

# Hardware

# Obniz

# CO2 sensor

- MH-Z19
- https://www.winsen-sensor.com/products/ndir-co2-sensor/mh-z19b.html
- command/response unofficial spec : https://revspace.nl/MHZ19#Command_0x86_.28read_concentration.29
- For serveral 10 seconds after power up, it sends out packets which obniz can safely ignore.

# LED

- Vf 1.9-2.4V
- If 20mA (max 30mA)
- 200 - 400 orm register shall be serialized

# Wiring

|MH-Z19 |Obniz|
|---|---|
| Vin (pin6) (3.6 - 5V) | 3 |
| GND (pin7)            | 4 |
| RxD (pin2) (0 / 3.3V) | 0 (TxD) |
| TxD (pin3) (0 / 3.3V) | 1 (RxD) |

|LED|Obniz|
|---|---|
| Anode | 10 |
| Cathode (maybe via 330ohm register) | 11 |
