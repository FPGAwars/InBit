# InBit
A hello world **Electron** and **node.js** application for setting a **bit** on or off from a GUI

![](wiki/v0.1/inbit-animation-01.gif)

## Why?

I wanted to learn a little bit about the **web technologies** for the **Desktop**. As I learn by doing, i decided to program this hello-world simple desktop webapp. I chose [Electron](https://electronjs.org/) because is the tool used for [Atom](https://atom.io/), my main editor. And of course, because all this tools are **Libre-software**

## How does it work?

When you turn the **GUI switch** on or off, the **DTR signal** from the **serial port** is changed. Im using it with the [Icezum Alhambra](https://github.com/FPGAwars/icezum/wiki) OpenFPGA board for sending bits from the Desktop to my circuits. Of course, it can also be used with any other **FTDI-based** board. The InBit app just opens a **serial port** and change the **DTR signal** according to the user inputs

The **hello-world** circuit that has been **uploaded** into the board in the above **animation** is the following:


![](wiki/v0.1//dtr-leds-circuit.png)

It simply shows the **DTR** and the inverted **DTR signals** on the LEDs 0 and 7 respectively

## Quick start

* Install [nodejs](https://nodejs.org)
* clone this repo:
```
git clone https://github.com/FPGAwars/InBit.git
```
* Enter into the working directory
```
cd InBit
```
* Install the npm packages:
```
npm install
```
* Edit the **renderer.js** and change the serial port name to the one you are using. By default the **/dev/ttyUSB1** is used
```javascript
var port = new serialport('/dev/ttyUSB1'  //--> Change /dev/ttyUSB1 for you serial port name
```
* Execute the app
```
npm start
```

## Documentation

Find more information in the [Wiki](https://github.com/FPGAwars/InBit/wiki) page (in Spanish)


## Contributing

Would you like to contribute?

* Create issues with bugs, features and so on
* Emit pull requests
* Add information to the wiki. Just click on the edit button and add information or fix the typos
* I do it on my spare time, so do not expect me to solve your questions or replying your messages immediately. Sometimes I have time. Sometimes not. Sorry for that. Just relax and enjoy. If you do not like the project, don't use it. But don't bother me.


## TODO
* Serial port error checking: no GUI messages are shown if there is an error with opening the serial port
* Add a serial port detector/selector to the GUI
* Package the app for the different platforms: linux, mac, windows
* Testing!
* Bug hunting!
* Learning! :-)

## License

* LGPL v3

## Author

* [Juan Gonzalez-Gomez](https://github.com/Obijuan) (Obijuan)
