<!-- 

    Hello!

    Please don't edit this file!

    If you'd like to make changes to the readme contents, please make them in the tpl/.readme.md file. If you'd like to add an example, please put the fil in eg/ and then add an entry to programs.json. To generate the markdown and update the main readme, run: 

    `grunt examples`







































-->
<img src="https://github.com/rwldrn/johnny-five/raw/master/assets/sgier-johnny-five.png">

# Node-isassemble Johnny-Five

_Artwork by [Mike Sgier](http://msgierillustration.com)_

[![Build Status](https://travis-ci.org/rwaldron/johnny-five.svg?branch=master)](https://travis-ci.org/rwaldron/johnny-five) [![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/rwaldron/johnny-five?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


#### Johnny-Five is an Open Source, Firmata Protocol based, IoT and Robotics programming framework, developed at [Bocoup](http://bocoup.com). Johnny-Five programs can be written for Arduino (all models), Electric Imp, Beagle Bone, Intel Galileo & Edison, Linino One, Pinoccio, Raspberry Pi, Spark Core, TI Launchpad and more!

Johnny-Five does not attempt to provide "all the things", but instead focuses on delivering robust, reality tested, highly composable APIs that behave consistently across all supported hardware platforms. Johnny-Five wants to be a baseline control kit for hardware projects, allowing you the freedom to build, grow and experiment with diverse JavaScript libraries of your own choice. Johnny-Five couples comfortably with: 

- Popular application libraries such as [Express.js](http://expressjs.com/) and [Socket.io](http://socket.io/).
- Fellow hardware projects like [ar-drone](https://github.com/felixge/node-ar-drone), [Aerogel](https://github.com/ceejbot/aerogel) and [Spheron](https://github.com/alchemycs/spheron)
- Bluetooth game controllers like [XBox Controller](https://github.com/andrew/node-xbox-controller) and [DualShock](https://github.com/rdepena/node-dualshock-controller)
- IoT frameworks, such as [Octoblu](http://www.octoblu.com/)

...And that's only a few of the many explorable possibilities. Check out these exciting projects: [node-pulsesensor](https://www.npmjs.org/package/node-pulsesensor), [footballbot-workshop-ui](https://www.npmjs.org/package/footballbot-workshop-ui), [nodebotui](https://www.npmjs.org/package/nodebotui), [dublin-disco](https://www.npmjs.org/package/dublin-disco), [node-slot-car-bot](https://www.npmjs.org/package/node-slot-car-bot), [servo-calibrator](https://www.npmjs.org/package/servo-calibrator), [node-ardx](https://www.npmjs.org/package/node-ardx), [nodebot-workshop](https://www.npmjs.org/package/nodebot-workshop), [phone-home](https://www.npmjs.org/package/phone-home), [purple-unicorn](https://www.npmjs.org/package/purple-unicorn), [webduino](https://www.npmjs.org/package/webduino), [leapduino](https://www.npmjs.org/package/leapduino), [lasercat-workshop](https://www.npmjs.org/package/lasercat-workshop), [simplesense](https://www.npmjs.org/package/simplesense), [five-redbot](https://www.npmjs.org/package/five-redbot), [robotnik](https://www.npmjs.org/package/robotnik), [the-blender](https://www.npmjs.org/package/the-blender)

## Supported Hardware

Johnny-Five has been tested on a variety of Arduino-compatible [Boards](https://github.com/rwaldron/johnny-five/wiki/Board).

For non-Arduino based projects, a number of platform-specific [IO Plugins](https://github.com/rwaldron/johnny-five/wiki/IO-Plugins) are available. IO Plugins allow Johnny-Five code to communicate with any non-Arduino based hardware in whatever language that platforms speaks!


#### Why JavaScript? [NodeBots: The Rise of JavaScript Robotics](http://www.voodootikigod.com/nodebots-the-rise-of-js-robotics)


## Supported Hardware

Johnny-Five has been tested on a variety of Arduino-compatible [Boards](https://github.com/rwaldron/johnny-five/wiki/Board).

For non-Arduino based projects, platform-specific [IO Plugins](https://github.com/rwaldron/johnny-five/wiki/IO-Plugins#available-io-plugins) are available. IO Plugins allow Johnny-Five code to communicate with any hardware in whatever language that platforms speaks! 


## Documentation

Documentation for the Johnny-Five API can be found [here](https://github.com/rwaldron/johnny-five/wiki) and [example programs here](https://github.com/rwaldron/johnny-five#example-programs). 

## Guidance

Need help? Ask a question on the [NodeBots Community Forum](http://forums.nodebots.io). If you just have a quick question or are interested in ongoing design discussions, join us in the [Johnny-Five Gitter Chat](https://gitter.im/rwaldron/johnny-five).

For step-by-step examples, including an electronics primer, check out [Arduino Experimenter's Guide for NodeJS](http://node-ardx.org/) by [@AnnaGerber](https://twitter.com/AnnaGerber)

Here is a list of [prerequisites](https://github.com/rwaldron/johnny-five/wiki/Prerequites) for Linux, OSX or Windows.

Check out the [bluetooth guide](https://github.com/rwaldron/johnny-five/wiki/JY-MCU-Bluetooth-Serial-Port-Module-Notes) if you want to remotely control your robot.

## Setup and Assemble Arduino

- Recommended Starting Kit: [Sparkfun Inventor's Kit](https://www.sparkfun.com/products/12001)
- Download [Arduino IDE](http://arduino.cc/en/main/software)
- Plug in your Arduino or Arduino compatible microcontroller via USB
- Open the Arduino IDE, select: File > Examples > Firmata > StandardFirmata
- Click the "Upload" button.

If the upload was successful, the board is now prepared and you can close the Arduino IDE.

For non-Arduino projects, each IO Plugin's repo will provide its own platform specific setup instructions.


## Hey you, here's Johnny!

#### Source Code:

``` bash
git clone git://github.com/rwldrn/johnny-five.git && cd johnny-five

npm install
```

#### npm package:

Install the module with:

```bash
npm install johnny-five
```


## Johnny-Five is...

```javascript
var five = require("johnny-five"),
    // or "./lib/johnny-five" when running from the source
    board = new five.Board();

board.on("ready", function() {

  // Create an Led on pin 13 and strobe it on/off
  // Optionally set the speed; defaults to 100ms
  (new five.Led(13)).strobe();

});
```
[Watch it here!](http://jsfiddle.net/rwaldron/dtudh/show/light)

> Note: Node will crash if you try to run johnny-five in the node REPL, but board instances will create their own contextual REPL. Put your script in a file.



## Many fragments. Some large, some small.

#### [Wireless Nodebot](http://jsfiddle.net/rwaldron/88M6b/show/light) NEW!
#### [Kinect Controlled Robot Arm](http://jsfiddle.net/rwaldron/XMsGQ/show/light/) NEW!
#### [Biped Nodebot](http://jsfiddle.net/rwaldron/WZkn5/show/light/)
#### [LCD Running Man](http://jsfiddle.net/rwaldron/xKwaU/show/light/)
#### [Slider Controlled Panning Servo](http://jsfiddle.net/rwaldron/kZakv/show/light/)
#### [Joystick Controlled Laser (pan/tilt) 1](http://jsfiddle.net/rwaldron/HPqms/show/light/)
#### [Joystick Controlled Laser (pan/tilt) 2](http://jsfiddle.net/rwaldron/YHb7A/show/light/)
#### [Joystick Controlled Claw](http://jsfiddle.net/rwaldron/6ZXFe/show/light/)
#### [Robot Claw](http://jsfiddle.net/rwaldron/CFSZJ/show/light/)
#### [Joystick, Motor & Led](http://jsfiddle.net/rwaldron/gADSz/show/light/)


## Example Programs
<!--extract-start:examples-->

### Board
- [Board](https://github.com/rwaldron/johnny-five/blob/master/docs/board.md)
- [Board With Port](https://github.com/rwaldron/johnny-five/blob/master/docs/board-with-port.md)
- [Board Multi](https://github.com/rwaldron/johnny-five/blob/master/docs/board-multi.md)
- [Repl](https://github.com/rwaldron/johnny-five/blob/master/docs/repl.md)
- [Pin](https://github.com/rwaldron/johnny-five/blob/master/docs/pin.md)

### LED
- [Led](https://github.com/rwaldron/johnny-five/blob/master/docs/led.md)
- [Led Blink](https://github.com/rwaldron/johnny-five/blob/master/docs/led-blink.md)
- [Led Pulse](https://github.com/rwaldron/johnny-five/blob/master/docs/led-pulse.md)
- [Led Fade](https://github.com/rwaldron/johnny-five/blob/master/docs/led-fade.md)
- [Led Fade Callback](https://github.com/rwaldron/johnny-five/blob/master/docs/led-fade-callback.md)
- [Led Status](https://github.com/rwaldron/johnny-five/blob/master/docs/led-status.md)
- [Led Array](https://github.com/rwaldron/johnny-five/blob/master/docs/led-array.md)
- [Led Rgb](https://github.com/rwaldron/johnny-five/blob/master/docs/led-rgb.md)
- [Led Rgb Anode](https://github.com/rwaldron/johnny-five/blob/master/docs/led-rgb-anode.md)
- [Led Rgb PCA9685](https://github.com/rwaldron/johnny-five/blob/master/docs/led-rgb-PCA9685.md)
- [Led Rainbow](https://github.com/rwaldron/johnny-five/blob/master/docs/led-rainbow.md)
- [Led Demo Sequence](https://github.com/rwaldron/johnny-five/blob/master/docs/led-demo-sequence.md)
- [Led Digits Clock](https://github.com/rwaldron/johnny-five/blob/master/docs/led-digits-clock.md)
- [Led Matrix](https://github.com/rwaldron/johnny-five/blob/master/docs/led-matrix.md)
- [Led Matrix Tutorial](https://github.com/rwaldron/johnny-five/blob/master/docs/led-matrix-tutorial.md)
- [Led Matrix HT16K33](https://github.com/rwaldron/johnny-five/blob/master/docs/led-matrix-HT16K33.md)
- [Led Matrix HT16K33 16x8](https://github.com/rwaldron/johnny-five/blob/master/docs/led-matrix-HT16K33-16x8.md)
- [Laser Trip Wire](https://github.com/rwaldron/johnny-five/blob/master/docs/laser-trip-wire.md)

### Servo
- [Servo](https://github.com/rwaldron/johnny-five/blob/master/docs/servo.md)
- [Servo Continuous](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-continuous.md)
- [Servo Slider](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-slider.md)
- [Servo Prompt](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-prompt.md)
- [Servo Drive](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-drive.md)
- [Servo Animation](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-animation.md)
- [Servo Array](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-array.md)
- [Servo PCA9685](https://github.com/rwaldron/johnny-five/blob/master/docs/servo-PCA9685.md)

### Servo Animation
- [Animation](https://github.com/rwaldron/johnny-five/blob/master/docs/animation.md)
- [Phoenix](https://github.com/rwaldron/johnny-five/blob/master/docs/phoenix.md)

### Motor
- [Motor](https://github.com/rwaldron/johnny-five/blob/master/docs/motor.md)
- [Motor Directional](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-directional.md)
- [Motor Brake](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-brake.md)
- [Motor Current](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-current.md)
- [Motor Hbridge](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-hbridge.md)
- [Motor PCA9685](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-PCA9685.md)
- [Motor 3 Pin](https://github.com/rwaldron/johnny-five/blob/master/docs/motor-3-pin.md)
- [Motobot](https://github.com/rwaldron/johnny-five/blob/master/docs/motobot.md)

### Stepper Motor
- [Stepper Driver](https://github.com/rwaldron/johnny-five/blob/master/docs/stepper-driver.md)
- [Stepper Sweep](https://github.com/rwaldron/johnny-five/blob/master/docs/stepper-sweep.md)

### ESC & Brushless Motor
- [Esc Keypress](https://github.com/rwaldron/johnny-five/blob/master/docs/esc-keypress.md)

### Sonar/Ultrasonic
- [Ping](https://github.com/rwaldron/johnny-five/blob/master/docs/ping.md)
- [Sonar Scan](https://github.com/rwaldron/johnny-five/blob/master/docs/sonar-scan.md)
- [Sonar](https://github.com/rwaldron/johnny-five/blob/master/docs/sonar.md)
- [Sonar I2c](https://github.com/rwaldron/johnny-five/blob/master/docs/sonar-i2c.md)

### Button
- [Button](https://github.com/rwaldron/johnny-five/blob/master/docs/button.md)
- [Button Bumper](https://github.com/rwaldron/johnny-five/blob/master/docs/button-bumper.md)
- [Button Options](https://github.com/rwaldron/johnny-five/blob/master/docs/button-options.md)
- [Button Pullup](https://github.com/rwaldron/johnny-five/blob/master/docs/button-pullup.md)

### Relay
- [Relay Lamp Controller](https://github.com/rwaldron/johnny-five/blob/master/docs/relay-lamp-controller.md)

### Shift Register
- [Shift Register](https://github.com/rwaldron/johnny-five/blob/master/docs/shift-register.md)
- [Shift Register Seven Segment](https://github.com/rwaldron/johnny-five/blob/master/docs/shift-register-seven-segment.md)

### Infrared (Proximity, Motion, Reflectance)
- [Ir Distance](https://github.com/rwaldron/johnny-five/blob/master/docs/ir-distance.md)
- [Ir Motion](https://github.com/rwaldron/johnny-five/blob/master/docs/ir-motion.md)
- [Ir Proximity](https://github.com/rwaldron/johnny-five/blob/master/docs/ir-proximity.md)
- [Proximity](https://github.com/rwaldron/johnny-five/blob/master/docs/proximity.md)
- [Ir Reflect](https://github.com/rwaldron/johnny-five/blob/master/docs/ir-reflect.md)
- [Ir Reflect Array](https://github.com/rwaldron/johnny-five/blob/master/docs/ir-reflect-array.md)

### Joystick
- [Joystick](https://github.com/rwaldron/johnny-five/blob/master/docs/joystick.md)
- [Joystick Claw](https://github.com/rwaldron/johnny-five/blob/master/docs/joystick-claw.md)
- [Joystick Laser](https://github.com/rwaldron/johnny-five/blob/master/docs/joystick-laser.md)
- [Joystick Motor Led](https://github.com/rwaldron/johnny-five/blob/master/docs/joystick-motor-led.md)

### LCD
- [Lcd](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd.md)
- [Lcd Enumeratechars](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-enumeratechars.md)
- [Lcd Runner 20x4](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-runner-20x4.md)
- [Lcd Runner](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-runner.md)
- [Lcd Runner](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-runner.md)
- [Lcd I2c](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-i2c.md)
- [Lcd I2c Runner](https://github.com/rwaldron/johnny-five/blob/master/docs/lcd-i2c-runner.md)

### Magnetometer (Compass)
- [Magnetometer Log](https://github.com/rwaldron/johnny-five/blob/master/docs/magnetometer-log.md)
- [Magnetometer North](https://github.com/rwaldron/johnny-five/blob/master/docs/magnetometer-north.md)
- [Magnetometer](https://github.com/rwaldron/johnny-five/blob/master/docs/magnetometer.md)

### Piezo
- [Piezo](https://github.com/rwaldron/johnny-five/blob/master/docs/piezo.md)

### IMU
- [Imu Mpu6050](https://github.com/rwaldron/johnny-five/blob/master/docs/imu-mpu6050.md)

### Sensors
- [Accelerometer](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer.md)
- [Accelerometer Adxl335](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer-adxl335.md)
- [Accelerometer Mma7361](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer-mma7361.md)
- [Accelerometer Mpu6050](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer-mpu6050.md)
- [Accelerometer Adxl345](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer-adxl345.md)
- [Accelerometer Pan Tilt](https://github.com/rwaldron/johnny-five/blob/master/docs/accelerometer-pan-tilt.md)
- [Gyro](https://github.com/rwaldron/johnny-five/blob/master/docs/gyro.md)
- [Gyro Mpu6050](https://github.com/rwaldron/johnny-five/blob/master/docs/gyro-mpu6050.md)
- [Photoresistor](https://github.com/rwaldron/johnny-five/blob/master/docs/photoresistor.md)
- [Photoresistor Servo](https://github.com/rwaldron/johnny-five/blob/master/docs/photoresistor-servo.md)
- [Potentiometer](https://github.com/rwaldron/johnny-five/blob/master/docs/potentiometer.md)
- [Sensor](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor.md)
- [Sensor Fsr Servo](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor-fsr-servo.md)
- [Sensor Fsr](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor-fsr.md)
- [Sensor Ir Led Receiver](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor-ir-led-receiver.md)
- [Sensor Slider](https://github.com/rwaldron/johnny-five/blob/master/docs/sensor-slider.md)
- [Slider Log](https://github.com/rwaldron/johnny-five/blob/master/docs/slider-log.md)
- [Slider Pan](https://github.com/rwaldron/johnny-five/blob/master/docs/slider-pan.md)
- [Slider Servo Control](https://github.com/rwaldron/johnny-five/blob/master/docs/slider-servo-control.md)
- [Temperature Tmp36](https://github.com/rwaldron/johnny-five/blob/master/docs/temperature-tmp36.md)
- [Temperature Lm35](https://github.com/rwaldron/johnny-five/blob/master/docs/temperature-lm35.md)
- [Temperature Ds18b20](https://github.com/rwaldron/johnny-five/blob/master/docs/temperature-ds18b20.md)
- [Temperature Mpu6050](https://github.com/rwaldron/johnny-five/blob/master/docs/temperature-mpu6050.md)

### Plugin Template
- [Plugin](https://github.com/rwaldron/johnny-five/blob/master/docs/plugin.md)

### Grove IoT Kit (Seeed Studio)
- [Grove Led](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-led.md)
- [Grove Button](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-button.md)
- [Grove Touch](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-touch.md)
- [Grove Sensor](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-sensor.md)
- [Grove Lcd Rgb](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-lcd-rgb.md)
- [Grove Lcd Rgb Temperature Display](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-lcd-rgb-temperature-display.md)
- [Grove Servo](https://github.com/rwaldron/johnny-five/blob/master/docs/grove-servo.md)

### TinkerKit
- [Tinkerkit Accelerometer](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-accelerometer.md)
- [Tinkerkit Blink](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-blink.md)
- [Tinkerkit Button](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-button.md)
- [Tinkerkit Continuous Servo](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-continuous-servo.md)
- [Tinkerkit Combo](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-combo.md)
- [Tinkerkit Gyroscope](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-gyroscope.md)
- [Tinkerkit Joystick](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-joystick.md)
- [Tinkerkit Linear Pot](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-linear-pot.md)
- [Tinkerkit Rotary](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-rotary.md)
- [Tinkerkit Thermistor](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-thermistor.md)
- [Tinkerkit Tilt](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-tilt.md)
- [Tinkerkit Touch](https://github.com/rwaldron/johnny-five/blob/master/docs/tinkerkit-touch.md)

### Wii
- [Nunchuk](https://github.com/rwaldron/johnny-five/blob/master/docs/nunchuk.md)
- [Classic Controller](https://github.com/rwaldron/johnny-five/blob/master/docs/classic-controller.md)

<!--extract-end:examples-->


## Contributing
All contributions must adhere to the [Idiomatic.js Style Guide](https://github.com/rwldrn/idiomatic.js),
by maintaining the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](https://github.com/gruntjs/grunt).


## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
