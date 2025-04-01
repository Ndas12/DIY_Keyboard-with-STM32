# STM32F407 Keyboard Interface with Push Buttons and LEDs

This project demonstrates how to interface a simple keyboard with the STM32F407 microcontroller using 4 push buttons as input keys and 4 LEDs as output indicators. When a button is pressed, the corresponding LED lights up, providing real-time feedback. This setup is ideal for understanding GPIO pin configuration and working with simple input/output systems on STM32 microcontrollers.

Project Overview:

In this system:

4 Push Buttons are used as input devices, each acting as a key in the keyboard interface.

4 LEDs are configured as output devices, where each LED corresponds to one of the push buttons. When a button is pressed, the corresponding LED will light up.

Key Features:
Real-time Interaction: The state of the buttons is constantly monitored, and the corresponding LED is turned ON when a button is pressed. If the button is released, the LED is turned OFF.

Debouncing Logic: To ensure reliable button presses, a debouncing mechanism is implemented to filter out any noise from the mechanical buttons.

Hardware Setup:
STM32F407 Microcontroller

4 Push Buttons connected to GPIO pins (configured as inputs)

4 LEDs connected to GPIO pins (configured as outputs)

Resistors for current limiting on LEDs 

How It Works:
The 4 push buttons are connected to the STM32F407's GPIO pins and configured as inputs with pull-down resistors to detect the button presses.

The 4 LEDs are connected to other GPIO pins, configured as outputs, to provide feedback when the associated button is pressed.

The firmware reads the state of each button and checks for a button press (active-low). When a button is pressed, the corresponding LED is turned ON. When the button is released, the LED turns OFF.

A basic debouncing algorithm ensures stable button press detection, preventing multiple unintended readings from a single press.

Applications:
This project can serve as the basis for more complex input/output systems, such as simple user interfaces or control systems with visual feedback.

