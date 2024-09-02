# SlimeVR Tracker firmware for ESP

Firmware for ESP8266 / ESP32 microcontrollers and different IMU sensors to use them as a vive-like trackers in VR.

Requires [SlimeVR Server](https://github.com/SlimeVR/SlimeVR-Server) to work with SteamVR and resolve pose.  

## Configuration

Make sure you are using sfusion branch for all LSM type trackers instead main.

Firmware configuration is located in the `defines.h` file. For more information on how to configure your firmware, refer to the [Configuring the firmware project section of SlimeVR documentation](https://docs.slimevr.dev/firmware/configuring-project.html).

## Compatibility

The following IMUs and their corresponding `IMU` values are supported by the firmware:

* BMI270 (IMU_BMI270), LSM6DSV (IMU_LSM6DSV), LSM6DSO (IMU_LSM6DSO), LSM6DSR (IMU_LSM6DSR)
  * Using common code: SoftFusionSensor for sensor fusion of Gyroscope and Accelerometer.
  * Gyro&Accel sample rate, gyroscope offset and 6-side accelerometer calibration supported.
  * In case of BMI270, gyroscope sensitivity auto-calibration (CRT) is additionally performed.

Firmware can work with both ESP8266 and ESP32. Please edit `defines.h` and set your pinout properly according to how you connected the IMU.

## Sensor calibration

For LSM6DSV six sides calibration and best practices see [Panda Trackers Readme](https://github.com/purraricat/SlimeVR-CheeseCake-PandaTrackers?tab=readme-ov-file)

## Contributions
Any contributions submitted for inclusion in this repository will be dual-licensed under
either:

- MIT License ([LICENSE-MIT](/LICENSE-MIT))
- Apache License, Version 2.0 ([LICENSE-APACHE](/LICENSE-APACHE))

Unless you explicitly state otherwise, any contribution intentionally submitted for
inclusion in the work by you, as defined in the Apache-2.0 license, shall be dual
licensed as above, without any additional terms or conditions.

You also certify that the code you have used is compatible with those licenses or is
authored by you. If you're doing so on your work time, you certify that your employer is
okay with this and that you are authorized to provide the above licenses.

For an explanation on how to contribute, see [`CONTRIBUTING.md`](CONTRIBUTING.md)
