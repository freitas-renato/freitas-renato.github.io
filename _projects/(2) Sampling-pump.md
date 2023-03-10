---
name: Air Sampling Pump
tools: [STM32, FreeRTOS, TouchGFX, C, C++, PID Control]
image: https://www.instrutherm.com.br/media/catalog/product/cache/1fff4d188f64e200d7e2f24d317b822f/b/o/bomba-de-amostragrem_2_.jpg
description: Air sampling pump to measure exposure to harmful dust, particulates and gases used for work safety.
---

# Air Sampling Pump

Developed for a client, personal sampling pumps play an important role in measuring exposure to harmful dust, particulates and gases. Frequently used in construction, industrial and emergency applications, personal sampling pumps help workers protect themselves and stay in compliance with various regulatory standards.

![bap-6000-case](https://www.instrutherm.com.br/media/catalog/product/cache/1fff4d188f64e200d7e2f24d317b822f/b/o/bomba-de-amostragrem_1_.jpg)

The project consisted of a main PCB powered by an STM32F4xx microcontroller used to control a small air pump (DC motor), maintaining the configured flow level steady for a long period of time (as long as 8 hours of constant use) using a **PID control loop**. The main challenge was to maintain a steady flow as the battery voltage decayed over time, thus a closed loop PID control.

The board was battery powered, and had also a 2.4-inch LCD display (RGB 656 interface) that allowed users to use an embedded GUI to configure measurements, view recorded data and manage equipment settings via a 4-button capacitive touch interface.

I helped to choose the main hardware components (microcontroller, flash, RAM, air pump, DC motor driver, LCD), reviewed EE schematics and PCB board design on Altium, and developed the entire firmware using C and C++: 
- GUI development using TouchGFX framework from STMicroelectronics
- Firmware architecture and development on FreeRTOS
- PID controller definition and tunning 
- Battery fuel gauge and charger control via I²C (Texas Instruments ICs)
- 4 button capacitive touch interface

Componets were chosen to make the product competitive in the Brazilian maket considering price and technologic difference from its competitors.

The whole project was developed in two years (2021-2022) and is being manufactured. You can find it on the client's website, a Brazilian measuring equipment vendor.

<p class="text-center">
{% include elements/button.html link="https://www.instrutherm.com.br/bomba-mod-bap-6000-de-amostragem-programavel-para-poeira-e-gases-display-colorido-e-tempo-de-ajuste-programavel-com-certificado-de-calibrac-o" text="Client's Page" %}
</p>



