# Interfacing STM32 with Stepper Motor using ULN2003 Motor Driver

## 🔍 Project Overview

This project demonstrates how to control a stepper motor with an STM32 microcontroller using the ULN2003 motor driver. We configure the STM32 to drive the stepper motor in both clockwise and counterclockwise directions. The motor can perform precise movements based on the specified steps and delay intervals.

## 🛠️ Hardware Requirements

- **STM32 Microcontroller (e.g., STM32F103)**
- **Stepper Motor** (28BYJ-48 or similar)
- **ULN2003 Motor Driver Module**
- **Power Supply** (as per motor specifications)
- Jumper wires and breadboard

### 📌 Pin Configuration

| STM32 Pin | ULN2003 Pin | Description  |
|-----------|-------------|--------------|
| PA1       | IN1         | Stepper Motor Input 1 |
| PA2       | IN2         | Stepper Motor Input 2 |
| PA3       | IN3         | Stepper Motor Input 3 |
| PA4       | IN4         | Stepper Motor Input 4 |

## 📂 Project Structure

- **`main.c`** - Contains the main code for controlling the stepper motor.
- **`stm32_hal_config.h`** - STM32 HAL configuration and pin definitions.
- **`tim.c`** - Timer configuration for creating microsecond delays.

## 💻 Software Requirements

- **STM32CubeIDE**
- **STM32 HAL Libraries**
- **ULN2003 Motor Driver Library** (custom code provided below)

## 📋 Code Explanation

### Functions

1. **microDelay** - Creates a microsecond delay using Timer1 (`TIM1`).
2. **move_clockwise** - Rotates the motor clockwise based on specified steps and delay.
3. **move_anticlockwise** - Rotates the motor counterclockwise based on specified steps and delay.


## 🚀 Getting Started

1. **Clone the Repository:**
   ```bash
   git clone <https://github.com/pratz222/STM32-Stepper-Motor-Interfacing>
   cd STM32-Stepper-Motor-Control
   ```

2. **Open Project in STM32CubeIDE:**
   - Open STM32CubeIDE, import the project folder, and ensure that the configurations for GPIO and TIM1 are correctly set.

3. **Build and Flash:**
   - Compile the code and flash it to your STM32 microcontroller.

4. **Connect the Hardware:**
   - Wire the stepper motor to the ULN2003 motor driver and connect it to the STM32 pins as specified.

## ⚙️ Configuration Notes

- **Timer Configuration:** Ensure that `TIM1` is configured in the STM32CubeMX for microsecond delays.
- **GPIO Initialization:** Initialize `IN1_PIN`, `IN2_PIN`, `IN3_PIN`, and `IN4_PIN` as output pins.

