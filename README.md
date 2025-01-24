# ESP32 LED Strip Controller with FreeRTOS, MQTT, and Predefined Patterns
This project allows an ESP32 microcontroller to control an addressable LED strip using MQTT messages. With FreeRTOS handling task management, it provides customizable RGB color control for individual LEDs and offers preset patterns such as Emergency, Christmas, and Knight Rider. The use of FreeRTOS ensures smooth operation, enabling simultaneous management of WiFi, MQTT communication, and LED updates.

## Features
WiFi Connectivity: Connects to a specified WiFi network.
MQTT Integration: Subscribes to an MQTT topic to receive LED control commands in JSON format.
Individual LED Control: Set color and brightness for each LED individually.
## Predefined Patterns:
### Emergency: All LEDs blink red with a 1-second interval.
### Christmas: Groups of 5 LEDs alternate between red and green, blinking every 500 ms.
### Knight Rider: A single LED "chaser" moves back and forth with a fading tail effect.
## Hardware Requirements
ESP32 Microcontroller
Adafruit NeoPixel LED Strip (or similar WS2812B-compatible addressable LED strip)
Power supply capable of powering both the ESP32 and LED strip
## Software Requirements
Arduino IDE (with ESP32 board support)
Adafruit NeoPixel Library
PubSubClient Library (for MQTT)
ArduinoJson Library
## Project Structure
The project is structured with FreeRTOS tasks to handle WiFi, MQTT, and LED control. Each LED pattern has a dedicated function for creating unique visual effects, triggered by commands sent via MQTT.
