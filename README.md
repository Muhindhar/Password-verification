# 🔐 Password Verification using TM4C123G, Keypad, and UART (PuTTY Interface)
This project demonstrates a password authentication system using the Tiva C Series TM4C123G microcontroller. A 4-digit password is entered through a 4x4 matrix keypad, and feedback is provided via UART0 using PuTTY. LED indicators show success or failure of the entered code.
## ✨ Features
- 4-digit password entry using a 4x4 matrix keypad
- UART communication via PuTTY (or any serial terminal)
- Password masking with asterisks (`*`)
- Green LED (Success), Red LED (Failure)
- Code customizable in source
## 🛠️ Hardware Required
- TM4C123GH6PM (Tiva C) LaunchPad
- 4x4 Matrix Keypad
- Jumper Wires
- USB Cable (for UART)
- LEDs (onboard PF1 - Red, PF3 - Green)
- Optional: Breadboard
## 💻 Software Required
- Keil uVision (for coding & flashing)
- PuTTY (or Tera Term) for serial communication
- TM4C123G header files & CMSIS library
## 📌 Pin Configuration

| Component     | MCU Pin      | Port | Direction | Description         |
|---------------|--------------|------|-----------|---------------------|
| Keypad Rows   | PE0 - PE3     | E    | Output    | Row control         |
| Keypad Columns| PC4 - PC7     | C    | Input     | Detect key press    |
| UART TX       | PA1           | A    | Output    | Transmit to PuTTY   |
| UART RX       | PA0           | A    | Input     | (Optional: receive) |
| Green LED     | PF3           | F    | Output    | Password correct    |
| Red LED       | PF1           | F    | Output    | Password incorrect  |
## 🚀 How It Works
1. Connect the keypad and LEDs to the TM4C123G as per the pin config.
2. Open PuTTY at 9600 baud rate, 8 data bits, no parity, 1 stop bit.
3. The user is prompted to enter a 4-digit password via the keypad.
4. Input is masked with `*` on PuTTY.
5. If the code matches the preset password (`2589`), green LED lights up and "SUCCESS" is displayed.
6. If the code is incorrect, red LED lights up and "FAILED" is shown.
7. The system resets after 2 seconds and prompts for input again.
## 🙌 Contributors
- Muhindhar (@Muhindhar)
- Inspired by embedded keypad/UART tutorials
🧑‍💻 Author
Muhindhar
KIOT - Department of ECE
