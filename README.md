LED Strip Control with MQTT
This program allows controlling a WS2811 LED strip with a "running horse" effect through MQTT messages from a broker.

It can work both on ESP32 and ESP8266 boards using the Arduino framework.

The main features:

Connects to WiFi network and MQTT broker
Subscribes to topics:
"home/ledstrip/state" - for on/off control
"home/ledstrip/brightness" - for brightness control
Initializes the WS2811 LED strip (Adafruit NeoPixel library)
In the main loop:
Checks for new MQTT messages
If state is ON:
Runs LED animation effect "on" - lights LEDs one by one
If state is OFF:
Runs LED animation effect "off" - turns off LEDs one by one
Sets LED colors using current brightness level
The "running horse" animation creates a smooth sequential effect
Brightness can be adjusted from 0 to 255 by publishing to MQTT topic
On/off state is controlled by publishing 1/0 to MQTT topic
Overall, this allows full control over a WS2811 LED strip - turn on/off, adjust brightness, with a nice animation effect.
