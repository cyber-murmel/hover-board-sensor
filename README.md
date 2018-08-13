# Hoverboard Sensorboard
This project is the reverse engineering of a hoverboard sensorboard.

## MPU
The microprocessor unit is a STM32F103C8T6 - the same processor as on the [Blue Pill dev board](https://wiki.stm32duino.com/index.php?title=Blue_Pill).

## IMU
The inertial measurement unit is a [MPU-6050](https://www.invensense.com/products/motion-tracking/6-axis/mpu-6050/) six-axis gyroscope + accelerometer attached via I²C.

## Voltage Converters
The +15 incoming voltage are converted to +5V via a [LM78M05](https://www.st.com/resource/en/datasheet/l78.pdf). The +5V are converted to +3.3V  via a [ASM1117-3.3](http://www.advanced-monolithic.com/pdf/ds1117.pdf). The whole setup is pretty yolo, since there is no cap stabilizing the +5V rail.

