# Smart Doorbell with ESPHome and Home Assistant Integration

Convert your traditional 12V doorbell into a smart doorbell with ESP8266/ESP32 and integrate it with Home Assistant using ESPHome.

This project allows you to control and monitor your doorbell through Home Assistant by detecting when the doorbell switch is pressed. When the switch is pressed, it triggers a relay, closing the circuit and ringing the doorbell.

## How It Works

1. **Traditional Circuit**: The traditional doorbell setup typically includes a 12V switch and a doorbell chime. When you press the switch, it closes the circuit, ringing the doorbell.
2. **ESP8266/ESP32 Integration**: We integrate an ESP8266 or ESP32 microcontroller with the existing doorbell circuit. The 12V switch is connected to one of the GPIO pins of the ESP board.
3. **Detecting Press**: The ESP8266/ESP32 detects when the switch is pressed using its internal GPIO pin (configured as an input). 
4. **Triggering Relay**: Once the switch press is detected, the ESP triggers a relay connected to the doorbell circuit. This closes the circuit, which rings the doorbell chime.
5. **Home Assistant Integration**: Through ESPHome, the doorbell press and relay can be monitored and controlled in Home Assistant. This allows automation, notifications, and control of the doorbell state.

## Wiring Diagram

1. **Switch**: The doorbell switch is connected to one of the ESP's GPIO pins (I've used D2 or GPIO4) and ground (configured as an input).
2. **Relay**: The relay is connected to another GPIO pin (I've used D7 or GPIO13), 3v And ground, which is used to control the relay that closes the doorbell circuit.

## Original doorbell diagram

<img width="550" alt="SCR-20240920-cqla" src="https://github.com/user-attachments/assets/02fd2a6f-4bad-4797-b101-13de7834a87c">

## Doorbell diagram with ESP & relay

<img width="574" alt="SCR-20240920-csrx" src="https://github.com/user-attachments/assets/a36b9a66-9345-4d70-ac2a-b73b4d6ac0d8">
