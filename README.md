# Analysis and Implementation of Embedded Operating Systems Lab 1

嵌入式作業系統分析與實作 Analysis and Implementation of Embedded Operating Systems [CSIE7618] @ NCKU 2022 Spring

## Development Environment

- Development Board
    - STM32F407G-DISC1
- Real-Time Operating System (RTOS)
    - [FreeRTOS v10.2.1](https://github.com/FreeRTOS/FreeRTOS/tree/V10.2.1)
- IDE
    - STM32CubeIDE

## Report

https://hackmd.io/@cpt/embeddedOS_lab1

## Requirement

- MultiTasking
    - Two tasks: one for LED controlling, the other for Button handling
    - Using Inter-Task Communication (ITC) mechanism
- LED-task has 2 states (S1, S2)
    - S1:
        - First, only Green LED lights up for 2 seconds,<br>and then only Red LED lights up for 2 seconds,<br>and then switches back to the Green LED, then RED, and so on
    - S2:
        - Only Orange LED is blinking (1 second ON, 1 second OFF, …)
- Button-task: If the button is pressed, the LED-task will switch to the other state (And execute from the start point of that state)
    - Debounce handling
    - Edge-detection handling