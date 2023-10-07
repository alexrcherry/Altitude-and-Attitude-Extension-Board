# Altitude-and-Attitude-Extension-Board
PCB design files for altitude and attitude extension board
## Purpose
The purpose of the Altitude and Attitude Extension Board is to measure the full state of a rocket. To do this, a gyroscope, accelerometer, gps, barometer and magnetometer are included on this board. A Kalman filter or some other means is necessary to get the full state of the rocket from the sensor data. The full state output of this board will be used to estimate the apogee of the rocket and to provide feedback for control systems.

| Requirement # | Requirement                                                                         | Justification                                                                                                                        | Testing Plan          |
| ------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | --------------------- |
| R-001         | Shall fit in 4” diameter body tube                                                  | PCB needs to fit into L1 kits & Olympus expected diameter.                                                                           | Measure with calipers |
| R-002         | Will use 2x M2 or larger mounting bolts                                             | Needs to be mounted easily inside the avionics bay.                                                                                  | X                     |
| R-003         | Will use 5v input power supply                                                      | The main power bus running the length of the rocket is 5v.                                                                           | X                     |
| R-004         | Will draw less than 1A                                                              | The device should not greatly affect the power bus for other devices. Current is limited so that voltage sag is minimized.           | X                     |
| R-005         | Will have 2x CAN high connection                                                    | Needs two connections so the device can be daisy chained.                                                                            | X                     |
| R-006         | Will have 2x CAN low connections                                                    | Needs two connections so the device can be daisy chained.                                                                            | X                     |
| R-007         | Will have 2x Gnd connections                                                        | Needs two connections so the device can be daisy chained.                                                                            | X                     |
| R-008         | Will have 2x 5v+ connections                                                        | Needs two connections so the device can be daisy chained.                                                                            | X                     |
| R-009         | Will fulfill the requirements across the temperature range of -90 to 50 deg C       | Needs to work in the sun on the launch pad and in the cold upper atmosphere.                                                         | Real conditions, freezer, oven?        |
| R-010         | Will use CAN 2.0                                                                    | Communication needs to be compatible with all other boards, can 2.0 chosen for high speed.                                           | X                     |
| R-011         | Should use STM32 microcontroller                                                    | This requirement is somewhat flexible, stm32 is greatly preferred because that is what the club currently has experience with.       | X                     |
| R-012         | Should have greater than 1 deg heading accuracy over flight time                    | This information may be used for active control and needs to be as accurate as possible to minimize rocket dispersion.               |                       |
| R-013         | Should be able to measure 10 g or greater acceleration                              | Testing will be done on solid rockets which generally have greater acceleration.                                                     |                       |
| R-014         | Should be able to measure altitude within < 5% error to 130km                       | Needs to measure altitude for a spaceshot. This may end up being done with radio ranging instead of IMU integration.                 |                       |
| R-015         | Should be able to detect launch, apogee, and landing                                | Software needs to send a signal to the main processing board for these important flight events so that logging rate can be modified. |                       |





