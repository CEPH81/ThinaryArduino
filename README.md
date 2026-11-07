# ThinaryArduino
 Thinary Development Board for Arduino

You can buy our product at this website:
https://thinaryelectronic.aliexpress.com

https://raw.githubusercontent.com/CEPH81/ThinaryArduino/master/Thinary-boards-index/package_thinary_index.json

1. Open Arduino IDE  ----->  File ------->   Preferences.

![image](https://github.com/Thinary/ThinaryArduino/blob/master/Image/1.png)

2. Open the URL editor.

![image](https://github.com/Thinary/ThinaryArduino/blob/master/Image/2.png)

3. Copy the URL to this Windows that Separate by Enter.

![image](https://github.com/Thinary/ThinaryArduino/blob/master/Image/3.png)

4. Open the Boards Manager, input Thinary to find. Than install “Thinary AVR Boards”.

![image](https://github.com/Thinary/ThinaryArduino/blob/master/Image/4.png)

5. Select the Thinary Nano Every and the Port, then use it the same as other Arduino Boards

![image](https://github.com/Thinary/ThinaryArduino/blob/master/Image/5.png)


## Version 1.0.1 (CEPH81 fork) - pin notes

| Function | Arduino pin | ATmega4808 |
|---|---|---|
| Serial (USB / CH340) | D2 TX, D3 RX | PA0 / PA1 (USART0) |
| Serial1 | D0 RX, D1 TX | PF1 / PF0 (USART2) |
| I2C (Wire) | **D4 SDA, D5 SCL** | PA2 / PA3 (A4/A5 cannot be I2C master) |
| SPI | D10 SS, D11 MOSI, D12 MISO, D13 SCK | PC3 / PC0 / PC1 / PC2 |
| PWM (analogWrite) | A0, A1, A2, A6, A7 | PD0-PD2 (TCA0), PF4 (TCB0), PF5 (TCB1) |
| Analog inputs | A0-A7 | AIN0-3, AIN12-15 |

tone() uses TCB1, so PWM on A7 stops while a tone is playing.
