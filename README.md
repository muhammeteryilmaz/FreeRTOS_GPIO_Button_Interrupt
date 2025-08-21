# FreeRTOS_GPIO_Button_Interrupt

## Description
This project demonstrates the use of a FreeRTOS binary semaphore to control an onboard LED with a button interrupt. Pressing the button on PC13 causes the LED on PB7 to turn on for 3 seconds and then turn off.

## FreeRTOS Features
- Binary semaphore (`xSemaphoreCreateBinary`, `xSemaphoreGiveFromISR`, `xSemaphoreTake`)
- Interrupt management (`portYIELD_FROM_ISR`)
- Task management (high-priority task)

## Hardware
- **Microcontroller**: STM32F446ZET6U
- **Button**: PC13 
- **LED**: Onboard LED on PB7

## Setup
1. Open the project in STM32CubeIDE.
2. Ensure FreeRTOS and HAL libraries are included.
3. Adjust PC13 as GPIO_EXTI13 and PB07 as GPIO_OUTPUT

## Outputs
- **LED**: The LED on PB7 lights up for 3 seconds when the button is pressed

## Test Results
- The button interrupt was successfully triggered, and the LED toggled as expected.
