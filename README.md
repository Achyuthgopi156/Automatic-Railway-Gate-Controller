
# Automatic Railway Gate Controller using 8051 Microcontroller

This project is an **Automatic Railway Gate Controller** using the 8051 microcontroller. The system automatically manages the opening and closing of the railway gate when a train is detected, ensuring both safety and efficiency by reducing the need for manual gate control.

## Project Overview

The system uses:
- Two **Infrared (IR) sensors** to detect the train's arrival and departure.
- A **L293D motor driver** to control the motor that opens and closes the gate.
- **Traffic lights** (Red and Green) to signal whether vehicles can pass or need to stop.

### How It Works:
1. **Initial State**: The green light is on, and the gate is open, allowing vehicles to pass.
2. **Train Approaching**: When the first IR sensor (IR1) detects a train, the system turns on the red light, turns off the green light, and closes the gate.
3. **Train Passing**: As the train continues and cuts the second IR sensor (IR2), the gate remains closed until the train has fully passed both sensors.
4. **Train Passed**: Once the train has cleared both sensors, the gate reopens, the red light turns off, and the green light turns back on, allowing vehicles to pass again.
5. The system repeats the process continuously, monitoring for trains.

## Circuit Components:
- 8051 Microcontroller
- 2 IR Sensors (for train detection)
- L293D Motor Driver (for gate control)
- DC Motor (to open and close the gate)
- LEDs (Green and Red traffic lights)
- Buzzer (for alarm)

## Code Explanation

The code is written in **Assembly language** for the 8051 microcontroller. It uses:
- **IR sensors** to detect the presence of the train.
- **Traffic light control** using GPIO pins.
- **Motor driver control** to operate the gate's DC motor.

### Key Functions
- `MotorForward`: Closes the gate when the train is detected.
- `MotorReverse`: Opens the gate when the train has passed.
- `DELAY` and `DELAY1`: Timers to control the gate motor's operation and light transition timings.

## Code Structure

The main loop consists of:
1. **IR sensor checks**: Continuously monitor the IR sensors to detect when a train approaches and departs.
2. **Motor control**: Operate the motor to open/close the gate based on sensor data.
3. **Traffic light control**: Manage red and green lights based on train position.

## Prerequisites

To work on this project, you will need:
- Basic knowledge of **Assembly language** for the 8051 microcontroller.
- An **8051 development kit** or emulator.
- Basic electronic components like IR sensors, LEDs, and a motor driver.

## Usage

1. Assemble the hardware as described.
2. Load the assembly code onto the 8051 microcontroller.
3. Test the system with a mock railway crossing.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

