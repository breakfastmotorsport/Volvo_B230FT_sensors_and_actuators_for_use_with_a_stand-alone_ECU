# Volvo-B230FT-sensors-and-actuators-for-use-with-a-stand-alone-ECU

Most components used by the LH-Jetronic 2.4 and EZ 116 K to control and regulate Volvo's B230FT are directly usable with a stand-alone engine-management system. Modern stand-alone ECUs benefit from upgrading the throttle position switch to a potentiometer-style throttle position sensor, swapping the narrow-band O2 sensor for a wide-band sensor (with controller) and adding manifold air pressure and inlet air temperature sensors.

This little collection of part numbers, pinouts and sensor values may help you setting up a stand-alone ECU or diagnose electrical issues.

*Please consider this to be incomplete and potentially inaccurate, especially when working with other variants of the Volvo Redblock or older versions of LH-Jetronic.*


## Sensors

### Engine speed sensor

Inductive speed sensor (variable reluctance/VR sensor). The flywheel has a 60-2 tooth pattern. Trigger is 90° before TDC (first tooth should be on 87° before TDC).

Part numbers:
* Volvo 271949
* Bosch 0 986 280 401

| Pin | Description |
| --- | --- |
| 1 | VR + |
| 2 | VR - |
| 3 | Shield/GND |

| Connector | Pin | Wire color |
| --- | --- | --- |
| EZK | 10 | R |
| EZK | 23 | BL |
| EZK | 11 | SB |

References:
* Volvo TP 0302057
* [Diagram 60-2 flywheel](Datasheets_and_other_helpful_documents/Engine_speed_sensor_-_60-2_flywheel.png)
* [Output pin 1 +](Datasheets_and_other_helpful_documents/Engine_speed_sensor_-_Negative_zero_crossing_on_tooth_- pin_1_+,_pin_2_-.png)
* [Output pin 1 -](Datasheets_and_other_helpful_documents/Engine_speed_sensor_-_Positive_zero_crossing_on_tooth_- pin_1_-,_pin_2_+.png)

### Engine coolant temperature sensor

Two NTC thermistors (R(25): ~2 kΩ; B(20/80): ~3510 K) are combined in one housing with two signal pins (for LH and EZK respectively) and GND through the thread. Thread size is M12x1.5.

Part numbers:
* Volvo 13 46 030
* Bosch 0 280 130 032

| Temperature | Resistance (between one pin and GND) |
| --- | --- |
| -10°C (14°F) | 8260-10560 Ω |
| +20°C (68°F) | 2280-2720 Ω |
| +80°C (176°F) | 290-364 Ω |

| Connector | Pin | Wire color |
| --- | --- | --- |
| LH | 13 | GR-W |
| EZK | 2 | R-SB |

References:
* Volvo TP 0302057

### Throttle position sensor (non-standard)

Potentiometer with linear characteristic curve. Used on Volvo 850 and others. [Adapter](https://yoshifab.com/store/b230-tps-adapter.html) for Redblocks commercially available.

Part numbers:
* Volvo 1336385
* Bosch 0 280 122 001

| Pin | Description |
| --- | --- |
| 1 | GND |
| 2 | IN (5V) |
| 3 | OUT |

References:
* [Technical product information on sensors](Datasheets_and_other_helpful_documents/Bosch_Sensors_[2001].pdf)

### Heated oxygen sensor (non-standard)

The Bosch LSU 4.9 wide-band O2 sensor with a suitable controller is currently the most common way to monitor air-fuel ratio.

Part numbers:
* Bosch 0 258 017 025 (or equivalent)

References:
* [Datasheet](Datasheets_and_other_helpful_documents/Bosch_0_258_017_025,_B_261_209_358-03_Lambda_Sensor_LSU_4.9 [2015].pdf)
* [Technical product information](Datasheets_and_other_helpful_documents/Bosch_Technical_Product_Information_- Planar_Wide_Band_Lambda_Sensor_-_LSU4.9_[2005].pdf)

### Intake air temperature sensor (non-standard)

NTC thermistor (R(25): ~2 kΩ; B(20/80): ~3531 K). Pins for signal and GND. Thread size is M12x1.5.

Part numbers:
* Bosch 0 280 130 039

| Temperature | Resistance |
| --- | --- |
| -10°C (14°F) | 15462 Ω |
| +20°C (68°F) | 2500 Ω |
| +80°C (176°F) | 323 Ω |

References:
* [Datasheet](Datasheets_and_other_helpful_documents/Bosch_0_280_130_039_Temperature_Sensor_NTC_M12-L_[2015].pdf)


## Actuators

### Injectors

Low resistance injectors. A resistor pack is used as standard. In simultaneous configuration with four injectors combined on one channel ~4 A are drawn.

Part numbers:
* Volvo 3517283
* Bosch 0 280 150 804

Flow rate at 3 bar: 300 cm³/min

| Connector | Pin | Wire color |
| --- | --- | --- |
| LH | 18 | GR |

References:
* Volvo TP 0302057

### Ignition discharge module

Fires the coil when the input signal goes from high (5 V) to low.

Part numbers:
* Volvo 3501921
* Bosch 0 227 100 124

| Pin | Description |
| --- | --- |
| 1 | Coil negative |
| 2 | GND (Kl. 31) |
| 3 | Input shield/GND |
| 4 | Coil positive |
| 5 | Input |
| 6 | NC |
| 7 | NC |

| Connector | Pin | Wire color |
| --- | --- | --- |
| EZK | 16 | GR |

References:
* Volvo TP 0302057

### System relay

Relay E. Contains fuel pump relay and enables it.

| Connector | Pin | Wire color |
| --- | --- | --- |
| LH | 21 | R |

References:
* Volvo TP 3904202

### Fuel pump relay

Relay E.

| Connector | Pin | Wire color |
| --- | --- | --- |
| LH | 20 | Y-SB |

References:
* Volvo TP 3904202


### Idle air control valve

Part numbers:
* Volvo 1389618
* Bosch 0 280 140 516

| Connector | Pin | Wire color |
| --- | --- | --- |
| LH | 33 | R-SB |

References:
* Volvo TP 0302057
