# ESP32_CAM_WebSocket_Servo_Tests
Test/example code for the ESP32-CAM to run servos via a PCA9685 servo driver over I2C

- Started with the [Autoconnect's FSBrowser example](https://github.com/Hieromon/AutoConnect/tree/master/examples/FSBrowser).
  - Allows automatic handling of WiFi access point selection.
  - Allows auto handling of web server set up.
- Added/modified websockets from [this example](https://github.com/acrobotic/Ai_Tips_ESP8266/tree/master/webserver_websockets).
  - Gives good basic websocket example code with no extra fluff.
- Added/modified [servo driver code](https://github.com/adafruit/Adafruit-PWM-Servo-Driver-Library/blob/master/examples/servo/servo.ino).
  - Allows driving 16 servos (expandable to more) with 2 pins (I2C).
- Added/modified HTML joysticks from [here](https://github.com/stemkoski/HTML-Joysticks).
  - Example webpage with 4 touchscreen joysticks without extra fluff.  Each joystick controls 2 servos
- Added/modified [inverse kinematics example](https://www.instructables.com/id/Arduino-Control-Robot-Arm-Via-Web/).
  - Example webpage with SVG arm picture to position arm.  Looks like a good way to control a robot arm via web page.
- Added/modified [Gamepad API example](https://github.com/luser/gamepadtest).
  - Example webpage that uses browser's Gamepad API to get joystick data.  Grab a joystick or game pad and control your robot.

# To Do:
- Add camera stream/capture.
- Add camera tracking features.
- Store joystick configuration.
- Add error handling to both ESP32 side and javascript side.
- Add socket closing/opening handling to both ESP32 side and javascript side.

# Hardware set up
- ESP32-CAM board
- PCA9685 board
- Serial board for programming

# Software set up
- Install Arduino IDE
- Install ESP32 board to board manager
- Install Autoconnect library (and its required dependancies)
- Install Websocket library
- Install Adafruit's PWM Servo Driver library
- Install [SPIFFS file uploader](https://github.com/me-no-dev/arduino-esp32fs-plugin).
- Compile and upload ESP32_CAM_WebSocket_Servo_Tests.ino
- Upload data directory to SPIFFS
- Play
