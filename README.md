# Adafruit MQTT Library

Modified Arduino library for MQTT supporting __larger data transfers__, including access to Adafruit IO.  Works with
the Adafruit FONA, Arduino Yun, ESP8266 Arduino platforms, and anything that supports
Arduino's Client interface (like Ethernet shield).

__This mod includes externally suppliable buffers via callback which can be greater than 65535 bytes.
For more info check the Adafruit_MQTT or Adafruit_MQTT_Client constructors.
The feature is active by default for ESP8266 and ESP32.

In addition there's a more flexible support for QoS and retained messages.
__


See included examples for how to use the library to access an MQTT service to
publish and subscribe to feeds.  Note that this does not support the full MQTT
spec but is intended to support enough for QoS 0 and 1 publishing.

Depends on the following other libraries depending on the target platform:

   - [Adafruit SleepyDog](https://github.com/adafruit/Adafruit_SleepyDog), watchdog
   library used by FONA code for reliability.

   - [Adafruit FONA](https://github.com/adafruit/Adafruit_FONA_Library), required for
   the FONA hardware.

Future todos:

   - Subscription callbacks

   - remove watchdog

<!-- START COMPATIBILITY TABLE -->

## Compatibility

MCU                | Tested Works | Doesn't Work | Not Tested  | Notes
------------------ | :----------: | :----------: | :---------: | -----
Atmega328 @ 16MHz  |             |             |     X       | 
Atmega328 @ 12MHz  |             |             |     X       | 
Atmega32u4 @ 16MHz |             |             |     X       | 
Atmega32u4 @ 8MHz  |             |             |     X       | 
ESP8266            |             |             |     X       | Active ext buffer via callback
ESP32              |      X      |             |             | Active ext buffer via callback
Atmega2560 @ 16MHz |             |             |     X       | 
ATSAM3X8E          |             |             |     X       | 
ATSAM21D           |             |             |     X       | 
ATSAMD51J20        |             |             |     X       |
ATtiny85 @ 16MHz   |             |             |     X       | 
ATtiny85 @ 8MHz    |             |             |     X       | 
Intel Curie @ 32MHz |            |             |     X       | 
STM32F2            |             |             |     X       |

  * ATmega328 @ 16MHz : Arduino UNO, Adafruit Pro Trinket 5V, Adafruit Metro 328, Adafruit Metro Mini
  * ATmega328 @ 12MHz : Adafruit Pro Trinket 3V
  * ATmega32u4 @ 16MHz : Arduino Leonardo, Arduino Micro, Arduino Yun, Teensy 2.0
  * ATmega32u4 @ 8MHz : Adafruit Flora, Bluefruit Micro
  * ESP8266 : Adafruit Huzzah
  * ATmega2560 @ 16MHz : Arduino Mega
  * ATSAM3X8E : Arduino Due
  * ATSAM21D : Arduino Zero, M0 Pro
  * ATSAMD51J20: Adafruit PyPortal
  * ATtiny85 @ 16MHz : Adafruit Trinket 5V
  * ATtiny85 @ 8MHz : Adafruit Gemma, Arduino Gemma, Adafruit Trinket 3V

<!-- END COMPATIBILITY TABLE -->
