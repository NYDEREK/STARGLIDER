<h1>STARGLIDER MainBoard rev1 - Datasheet</h1>

<h2>Main Board Features</h2>
<img src="https://github.com/user-attachments/assets/6677b421-2b84-42e9-8078-9319c81048de" alt="Main Board Features" width="600">

<ul>
  <li>STM32G474RET6 microcontroller in LQFP64 package</li>
  <li>RGB LED diode</li>
  <li>JST SH SM0XB SSR TB connectors</li>
  <li>MIPI10 - STDC14 programmer connector</li>
  <li>Tag connector programmer footprint</li>
  <li>Micro SD card slot</li>
  <li>Buzzer</li>
  <li>BME280 Temperature, Humidity &amp; Pressure sensor</li>
  <li>LSM6DS3 Accelerometer &amp; Gyroscope IMU module</li>
  <li>USB 2.0 connector</li>
</ul>

<h2>Description</h2>
<p>
Main Board is the most important PCB in the STARGLIDER build.  
It controls all other modules, saves data on the micro-SD card, calculates flight data 
such as attitude, roll, pitch, and yaw, and measures Temperature, Humidity, and Pressure.  
Thanks to the built-in “Cordic” it is able to easily calculate flight path &amp; Kalman filter.
</p>

<h2>Main Board Pinout</h2>
<img src="https://github.com/user-attachments/assets/32504bdd-b91b-4b3a-a530-6b0dd5c1b1e3" alt="Main Board Pinout" width="600">

<p>
The Main Board provides 6 different connectors for GPIO, ADC, PWM, Communication, and one connector for Power.  
Input voltage range: <strong>5 – 9 V</strong>.  
Current consumption without external peripherals: <strong>&lt; 1A</strong>.  
Logic pin voltage should not exceed <strong>3.3V</strong>.  
</p>
<p>
Board capabilities include Low-power UART to LSM6DS3 IMU (U7).  
More information is available in the schematic provided in the project files.
</p>

<h2>Programming</h2>
<img src="https://github.com/user-attachments/assets/b1ac0870-535c-45d1-acd8-f721533cdcc8" alt="Programming Connections" width="300">

<p>Main Board can be programmed by ST-Link from STMicroelectronics.</p>
<p>Supported development toolchains:</p>
<ul>
  <li>IAR Systems® – IAR Embedded Workbench®</li>
  <li>Keil® – MDK-ARM</li>
  <li>STMicroelectronics – STM32CubeIDE</li>
</ul>

<h2>Measurements</h2>
<p>Main Board is able to measure:</p>
<ul>
  <li>Accelerations</li>
  <li>Angular velocity</li>
  <li>Temperature</li>
  <li>Humidity</li>
  <li>Pressure</li>
  <li>Voltage</li>
</ul>

<h2>LSM6DS3</h2>
<img src="https://github.com/user-attachments/assets/f199631d-80e0-4dee-909f-c00153c1bbcc" alt="LSM6DS3 Accelerometer &amp; Gyroscope" width="600">
<p>
The LSM6DS3TR-C is a system-in-package featuring a 3D digital accelerometer and a 3D digital gyroscope.  
It performs at 0.90 mA in high-performance mode and enables always-on low-power features.  
</p>
<p>
Acceleration range: ±2/±4/±8/±16 g<br>
Angular rate range: ±125/±250/±500/±1000/±2000 dps
</p>

<h2>BME280</h2>
<img src="https://github.com/user-attachments/assets/c9f66a39-eb9d-4c67-9476-8c052cc9ca83" alt="BME280 Sensor" width="300">

<p>
The BME280 is a combined digital humidity, pressure, and temperature sensor.  
It provides fast response time, high accuracy over a wide temperature range, and optimized low-noise temperature sensing.  
</p>
<p>
Pressure sensor: absolute barometric, high accuracy, lower noise than BMP180.<br>
Temperature output: used for compensation of pressure &amp; humidity, also for ambient temperature estimation.
</p>

<h2>Analog to Digital Converter (ADC)</h2>
<p>The STM32G474RET6 includes 5 successive approximation ADCs with:</p>
<ul>
  <li>12-bit native resolution, built-in calibration</li>
  <li>Up to 4 Msps conversion rate (25 ns sampling time)</li>
  <li>Up to 6.66 Msps at 6-bit resolution</li>
</ul>
<p>
The MCU performance allows the Main Board to measure voltages in the 0 – 3.3 V range with high resolution and speed.
</p>
