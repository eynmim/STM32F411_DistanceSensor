# STM32F411_DistanceSensor
STM32F411 Nucleo project using an ultrasonic sensor to measure distance, displayed in centimeters on a 2x16 LCD. The LCD is directly interfaced without additional modules. All project files, including source code and setup details, are provided for easy replication and understanding.
 
This project leverages the STM32F411 Nucleo board to create a simple yet effective distance measurement system using an ultrasonic sensor. The measured distance is displayed in real-time on a 2x16 character LCD screen, with the values shown in centimeters.

Key features of this project include:


This project serves as an excellent starting point for those looking to explore embedded systems with STM32 microcontrollers, offering hands-on experience with sensor integration and display interfacing.

1. Hardware Requirements:
   
            - Microcontroller Board: STM32F411 Nucleo
            - Ultrasonic Sensor: [Specify the model, e.g., HC-SR04]
            - LCD Display: 2x16 Character LCD (HD44780 compatible) without the need for additional driver modules.
            - Power Supply: [Specify voltage, e.g., 5V, 3.3V]
            - Connecting Wires
            - Breadboard (optional)
3. Software Requirements:
   
            - IDE: [e.g., STM32CubeIDE, Keil uVision]
            - Toolchain: GCC for ARM (or the toolchain associated with your IDE)
            - STM32CubeMX: [Specify version if used for pin configuration]
            - Firmware Package: STM32F4 HAL drivers [Specify version if applicable]
5. Pin Configuration:
   
            Ultrasonic Sensor Connections:
              - Trigger Pin: PA10 (D2)
              - Echo Pin: PA4 (A2)
            LCD Display Connections:
              - RS (Register Select): PB5 (D4)
              - E (Enable): PB4 (D5)
              - D4-D7 (Data Lines): PC7 (D9), PB6 (D10), PA7 (D11), PA6 (D12)
            Power and Ground:
              - VCC: 5V 
              - GND (on microcontroller) : Vss , V0 , RW , K (on LCD) , GND(on Ultrasonic)
              - 3V3 : A
7. Clock Configuration:
   
            - System Clock Source: HSE (High-Speed External)
            - SYSCLK (System Clock Frequency): 100 MHz
            - APB1 (Low-Speed Peripheral Clock): 50 MHz
            - APB2 (High-Speed Peripheral Clock): 100 MHz
9. Peripheral Configuration:
    
            GPIO:
            - Mode: Output for LCD control and Trigger Pin
            - Mode: Input for Echo Pin
            Timers:
            - Tim2 : Clock source set to "Internal Clock"
            I2C : set to ON (PB8 as SCL and PB7 as SDA)

11. Testing and Debugging
    
            Initial Power-On Test:
            - Verify that the LCD initializes correctly and displays a welcome message.
            - Sensor Functionality:
            - Test the ultrasonic sensor by placing an object at a known distance and verifying the displayed value.
          




