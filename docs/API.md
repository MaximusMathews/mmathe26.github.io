---
Title: API
---

## Messages Passed on
### Message Type 1 (Wifi Toggle - Auto/Manual)

<b><i>Used to toggle stepper motor from automatic (state 0) to manual (state 1).</i></b>

|               | Byte 1      |  
|---------------|-------------|
| Variable Name | auto_toggle |   
| Variable Type | uint8_t     |   
| Min Value     | 0           |   
| Max Value     | 1           |   
| Example       | 0           |   

### Message Type 4 (Button - digital signal)

<b><i>Used to manually control stepper motors from left to right. It has two states (0) and (1) to determine if the button has been pressed.</i></b>

|               | Byte 1      | Byte 2       |
|---------------|-------------|--------------|
| Variable Name | button_left | button_right |
| Variable Type | uint8_t     | uint8_t      |
| Min Value     | 0           | 0            |
| Max Value     | 1           | 1            |
| Example       | 0           | 1            |

## Messages Sent
### Message Type 2 (Optical Sensor Readings)

<b><i>The light levels will be sent to the motor subsystem to automatically control the solar cell to face the most optimal position to generate power. The readings will have a range of lux between 0-9999.</i></b>

|               | Byte 1-2   | Byte 3-6   | Byte 7-8   | Byte 9-12  | Byte 13-14   | Byte 15-18 | Byte 19-20  | Byte 21-24 |
|---------------|------------|------------|------------|------------|--------------|------------|-------------|------------|
| Variable Name | sensor_one | L1_Reading | sensor_two | L2_Reading | sensor_three | L3_Reading | sensor_four | L4_Reading |
| Variable Type | char       | float      | char       | float      | char         | float      | char        | float      |
| Min Value     | L1         | 0          | L2         | 0          | L3           | 0          | L4          | 0          |
| Max Value     | L1         | 9999       | L2         | 9999       | L3           | 9999       | L4          | 9999       |
| Example       | L1         | 3567       | L2         | 2343       | L3           | 1232       | L4          | 2142       |


### Message Type 3 (Voltage Readings from Solar Panel)

<b><i>Received and Forwarded to MQTT</i></b>

|               | Byte 1         | Byte 2-5        |
|---------------|----------------|-----------------|
| Variable Name | voltage_sensor | voltage_reading |
| Variable Type | char           | float           |
| Min Value     | V              | 0.000           |
| Max Value     | V              | 5.500           |
| Example       | V              | 3.400           |
