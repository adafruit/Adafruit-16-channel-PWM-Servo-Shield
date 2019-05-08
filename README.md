# PCB for the Adafruit 16-channel PWM/Servo shield

__Format is EagleCAD schematic and board layout__

<a href="http://www.adafruit.com/products/1411"><img src="assets/image.jpg?raw=true" width="500px"><br/>Click here to purchase one from the Adafruit shop</a>

You want to make a cool Arduino robot, maybe a hexapod walker, or maybe just a piece of art with a lot of moving parts. Or maybe you want to drive a lot of LEDs with precise PWM output. Then you realize that the Arduino has only a few PWM outputs, and maybe those outputs are conflicting with another shield! What now? You could give up OR you could just get our handy PWM and Servo driver shield. It's just like our popular PWM/Servo Breakout but now Arduino-ready and works with any Arduino that uses shields: Uno, Leo, Mega, ADK, its all good.

When we saw this chip, we quickly realized what an excellent add-on this would be. __Using only two I2C pins, control 16 free-running PWM outputs!__ You can even stack up 62 shields to control up to 992 PWM outputs (which we would really like to see since it would be glorious and like 4 feet tall) Because I2C is a shared bus you can also connect other I2C devices and sensors to the SCL/SDA pins as long as their addresses don't conflict (this shield has address 0x40)

- There's an I2C-controlled PWM driver with a built in clock. That means that, unlike the TLC5940 family, you do not need to continuously send it signal tying up your microcontroller, its completely free running!
- It is 5V compliant, which means you can control it from a 3.3V Arduino and still safely drive up to 6V outputs (this is good for when you want to control white or blue LEDs with 3.4+ forward voltages)
- 6 address select pins so you can stack up to 62 of these on a single i2c bus. 12 out of 16 output pins can be accessed when stacked.
- Adjustable frequency PWM up to about 1.6 KHz
- 12-bit resolution for each output - for servos, that means about 4us resolution at 60Hz update rate
- Configurable push-pull or open-drain output

We wrapped up this lovely chip into a shield with a couple nice extras

- Terminal block for power input (or you can use the 0.1" breakouts on the side)
- Reverse polarity protection on the terminal block input
- Green and red power-good LEDs
- 3 pin connectors in groups of 4 so you can plug in 16 servos at once (Servo plugs are slightly wider than 0.1" so you can only stack 4 next to each other on 0.1" header
- Stackable design. You'll need to pick up stacking headers and right angle 3x4 headers in order to stack on top of this shield without the servo connections getting in the way.
- A spot to place a big capacitor on the V+ line (in case you need it)
- 220 ohm series resistors on all the output lines to protect them, and to make driving LEDs trivial
- Solder jumpers for the 6 address select pins
- A lot of extra space remaining? Let's turn it into a prototyping area. You get a 5x20 proto area for any extra wiring you'd like to add

This product comes with a fully tested and assembled shield as well as 4 pieces of 3x4 male straight header (for servo/LED plugs), a 2-pin terminal block (for power) and a stick of 0.1" header so you can plug into an Arduino. A little light soldering will be required to assemble and customize the board by attaching the desired headers but it is a 15 minute task that even a beginner can do. [If you want to use right-angle 3x4 headers, we also carry a 4 pack in the shop - note that only 3 of them can be used when stacking (12 servos total)](http://www.adafruit.com/products/816).

__Servos and Arduino not included__ - but we do sell tons of different servos in the shop so pick up a few while you're here!

## License

Adafruit invests time and resources providing this open source design, 
please support Adafruit and open-source hardware by purchasing 
products from Adafruit!

Designed by Adafruit Industries.  
Creative Commons Attribution, Share-Alike license, check license.txt for more information
All text above must be included in any redistribution
