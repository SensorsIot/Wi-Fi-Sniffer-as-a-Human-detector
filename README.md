# Wi-Fi Sniffer as a Human detector

This is the Material for video: https://www.youtube.com/watch?v=fmhjtzmLrg8

Things to do before you start:
- In mqtt.h update mqttServer = "Your Broker IP address"
- replace MQTT_USERNAME, MQTT_KEY if you do not use Peter Scargills script or you changed the "admin, admin".
- In WiFi_Sniffer set mySSID and MyPassword
- The mqtt topic is Sniffer/#

You find a sample Node-Red flow. Just copy-paste the raw file into your Node-Red


# Dependencies

Install using the Library Manager in Arduino:
- ESP8266
- ArduinoJson ( https://bblanchon.github.io/ArduinoJson/ )
- PubSubClient ( https://pubsubclient.knolleary.net )
