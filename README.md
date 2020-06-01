# Raspberry-Pi-Serial-Communication

  Unlike Arduino boards, if you want to do serial communication using Raspberry Pi boards, you must do some settings. 
  To know about the Serial Ports of your Raspberry Pi board, must read this [link-1](https://www.raspberrypi.org/documentation/configuration/uart.md)

  The method and code of serial communication can be found here in [link-2](https://www.electronicwings.com/raspberry-pi/raspberry-pi-uart-communication-using-python-and-c)

  From **link-1**, you will know where do the Tx and Rx pins of Raspberry Pi maps, and how to map them to UART0.

  **Link-2** will guide you through the wiring and other setup needed to establish serial communication.

  While testing, i used **Pololu Serial Transmitter utility for Windows**. It can be downloaded from [here](https://www.pololu.com/docs/0J23)
  You can use any Serial Terminal for testing the Raspberry Pi serial connection.
  
# Note that:
 
   After successfully following the documentation and setting in link-1, when you write:

        $ ls -l /dev

   whatever comes infront of serial0 is the where your Tx/Rx pins are mapped now. In my case it was:

   **serial0 -> ttyAMA0** ; and **serial1 -> ttyS0**
  
   Therefore, while writing code for serial read/write in Raspberrt Pi, I have used **ttyAMA0** where needed.
