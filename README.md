# 🏠 Smart Home Automation with Google Assistant, IR Remote, Alexa, SinricPro Website & Mannual
Using NodeMCU ESP8266, Arduino UNO & Sinric Pro

---

## 🚀 Project Overview  
Control your home appliances with Google Assistant, Amazon Alexa, IR Remote, and manual switches! No need for expensive hardware like Echo Dot or Nest Mini. Manage your devices remotely or offline with this free and easy-to-build IoT smart home system.

---

## 🌟 Features  
- 🗣️ Voice control via Google Assistant & Alexa  
- 📱 Control with Sinric Pro Dashboard and mobile apps  
- 🔄 Real-time appliance status feedback  
- 🎛️ Manual control with physical switches & IR remote  
- 💾 EEPROM state memory to retain device status after power off  
- 💸 All tools and APIs free for up to 3 devices  

---

## 📋 Table of Contents  
- [Introduction](#-introduction)  
- [SPDT Switch Uses](#-spdt-switch-uses)  
- [Circuit Diagram](#-circuit-diagram)  
- [Required Components](#-required-components)  
- [Sinric Pro Account Setup](#-sinric-pro-account-setup)  
- [Programming NodeMCU](#-programming-nodemcu)  
- [Connecting Sinric Pro with Alexa](#-connecting-sinric-pro-with-alexa)  
- [Adding Devices in Alexa App](#-adding-devices-in-alexa-app)  
- [Creating a Home in Google Home App](#-creating-a-home-in-google-home-app)  
- [Connecting Sinric Pro with Google Home](#-connecting-sinric-pro-with-google-home)  
- [Controlling Devices via Google Assistant](#-controlling-devices-via-google-assistant)  
- [Getting IR HEX Codes from Remote](#-getting-ir-hex-codes-from-remote)  
- [Programming Arduino UNO](#-programming-arduino-uno)  
- [NodeMCU Relay Control via Voice](#-nodemcu-relay-control-via-voice)  
- [Manual Relay Control](#-manual-relay-control)  
- [Project Completion](#-project-completion)  

---

## 📖 Introduction  
In this IoT project, control 3 home appliances from anywhere using voice or manually. The NodeMCU connects with Sinric Pro for cloud control via Alexa and Google Assistant. Manual switches and IR remote can be used in offline mode.

---

## 🔀 SPDT Switch Uses  
This switch toggles power between NodeMCU and Arduino UNO to select control mode:  
⚡ NodeMCU ON: Control via Alexa, Google Assistant, Sinric Pro  
⚡ Arduino UNO ON: Control via IR remote & manual switches  

---

## 🔌 Circuit Diagram  
- NodeMCU GPIO D1, D2, D5, D6 connected to 4-channel relay module  
- Manual switches connected to SD3, D3, D7, RX GPIO pins  
- Use 5V 2A power supply  
⚠️ Ensure manual switches S1 & S2 are OFF during NodeMCU boot to prevent boot failure.  

*![Circuit Diagram Placeholder](.Circuit_Diagram.png)*  

---

## 🛠️ Required Components  
- NodeMCU ESP8266  
- Arduino UNO  
- 4-channel 5V SPDT Relay Module  
- Manual switches & SPDT switch  
- IR Receiver sensor  
- 5V 2A Power supply  
- Connecting wires, bulbs, sockets  
- (Optional) Amazon Echo Dot / Google Nest Mini  

---

## 🌐 Sinric Pro Account Setup  
1. Register at [sinric.pro/register](https://sinric.pro/register) (3 devices free)  
2. Create rooms and devices in Sinric dashboard  
3. Note API Key, Secret & Device IDs for firmware  

---

## 💻 Programming NodeMCU  
- Update Arduino IDE with ESP8266 board manager URLs  
- Install ESP8266 board package  
- Install required libraries:  
  - Sinric Pro  
  - WebSockets (≥2.3.5)  
  - ArduinoJson (≥6.12.0)  
- Insert WiFi & Sinric credentials into code  
- Upload program to NodeMCU  

---

## 📲 Connecting Sinric Pro with Alexa  
- Enable Sinric Pro skill in Alexa app  
- Link Sinric account  
- Discover devices  
- Use voice commands like:  
  `"Alexa, turn on Room Light"`  

---

## 📱 Adding Devices in Alexa App  
Devices created in Sinric Pro appear under Smart Home > Devices in Alexa app.

---

## 🏠 Creating a Home in Google Home App  
- Install Google Home app  
- Create new home & assign a nickname  
- Add devices once home is ready  

---

## 🔗 Connecting Sinric Pro with Google Home  
- Link Sinric Pro account via "Works with Google" in Google Home  
- Devices become accessible for voice/app control  

---

## 🎙️ Controlling Devices via Google Assistant  
Use commands like:  
`"Hey Google, turn on the Room Light"`  
Monitor device status remotely with Google Home app.

---

## 📡 Getting IR HEX Codes from Remote  
- Wire IR receiver OUT to Arduino UNO A0 pin  
- Use IRremote v3.6.1 library in Arduino IDE  
- Upload IR capture sketch  
- Press remote buttons; note HEX codes from Serial Monitor  
- Update main Arduino sketch with HEX codes  

---

## 🤖 Programming Arduino UNO  
- Install libraries: IRremote, AceButton, Arduino-timer  
- Upload relay & IR remote control sketch to Arduino UNO  

---

## 🕹️ NodeMCU Relay Control via Voice  
If connected to WiFi and Sinric Pro, control relays with Alexa or Google Assistant. Status updates reflect instantly in apps.

---

## 🔧 Manual Relay Control  
Switches or pushbuttons provide offline/manual control. Status syncs when devices reconnect to WiFi.

---

## 🎉 Project Completion  
Your Sinric Pro smart home system is now ready! Enjoy smart and manual control combined in one efficient IoT project.

---

## 👏 Credits  
- Prof. Birbal Kumar Rajak (HoD, Electronics)  
- Prof. Muneswar Kumar (Mentor)  
- Prashant Kumar (Co-Mentor)  
- Team: Sushant Sagar, Aditya Bharti, Gourav Kumar, Ankit Kumar, Sujit Kumar, Siddhant Kumar  

---

✨ Feel free to contribute, ask questions, or provide feedback! ✨
