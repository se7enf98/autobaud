A sketch that determines the baud rate of UART communication by measuring pulses using input capture. Input capture is a feature that copies the value of a timer to a register when a pin gets high or low, making it possible to precisely time signals. This sketch registers the time of a falling edge, and then the time of a rising edge. The difference is the duration of a pulse. This is measured five times and the minimum length is printed on the serial line.

Currently this works on an Arduino Uno and possibly on other boards based on the ATmega328. Pin 8 is used to measure pulse duration, so connect pin 8 to the UART and connect the GND of the Arduino to the GND of the device. Then, connect the serial monitor on 115200 bps and the sketch will tell you the baud rate of the UART that it is connected to on pin 8.