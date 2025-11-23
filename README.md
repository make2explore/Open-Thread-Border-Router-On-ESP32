## OpenThread Border Router on ESP32  
  
<img src="/Images/m2e-OTBR-32s.jpg" height="200"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <img src="/Images/m2e-OTBR-32-c6.jpg" height="200" >

  
An **OTBR**, or **OpenThread Border Router**, is the open-source implementation of a Thread Border Router that acts as a gateway, connecting a Thread network (a low-power wireless mesh protocol for IoT) to external IP-based networks like the internet or Wi-Fi. It provides essential services such as IP connectivity, service discovery, and external commissioning, allowing Thread devices to communicate with services and devices beyond the Thread network, which is crucial for smart home ecosystems like Matter.  
  
Building an OpenThread Border Router (OTBR) on an ESP32 requires a **two-chip architecture** because a standard ESP32 lacks the necessary IEEE 802.15.4 radio for Thread networking. The setup involves a Wi-Fi-capable ESP32 board, such as the ESP32-S3, to act as the host processor and a separate chip with an 802.15.4 radio, like the ESP32-H2, to function as the Radio Co-Processor (RCP). This dual-chip design allows the host ESP32 to handle the high-level border router tasks while the RCP manages the low-level Thread network communications. To simplify this, Espressif offers a dedicated development board, though a DIY setup with a standard ESP32 and an external RCP is also an option.  

The software-based setup uses Espressif's IoT Development Framework (ESP-IDF) and their ESP Thread Border Router SDK to compile and flash the necessary firmware. Developers first build and flash the RCP firmware onto the 802.15.4 chip. Then, they configure and flash the main border router firmware onto the host ESP32, which enables network-bridging capabilities. The process is guided by the ESP-IDF command-line interface, allowing developers to configure network settings and manage the Thread network from the serial monitor once the device is running.  
  
### Prerequisites 🧰
  
To set the OpenThread Border Router (OTBR) using a ESP32, there are following Hardware-software Prerequisites - 
  
### Hardware  
The core of an ESP32-based OTBR is a two-chip setup, combining a Wi-Fi-capable host with a dedicated radio co-processor (RCP).
- Host processor: A Wi-Fi-enabled ESP32 series chip, such as the ESP32, ESP32-S3, or ESP32-C3, to run the main OpenThread stack and connect to the internet.
- Radio Co-Processor (RCP): An ESP32-H series chip (like the ESP32-H2) with an integrated IEEE 802.15.4 radio to manage the physical layer of the Thread network. The communication between the host and the RCP is typically handled via a UART or SPI interface.  
- Integrated solution (optional): For simplicity, Espressif offers a specialized development board, such as the ESP Thread Border Router/Zigbee Gateway board, that combines the ESP32-S3 host and ESP32-H2 RCP on a single module. This removes the need for manual wiring between separate chips.  
  
### Software  
- ESP-IDF: Espressif's official IoT Development Framework is the foundation for compiling and flashing firmware to the ESP32 chips.
- ESP Thread Border Router SDK: This official SDK from Espressif builds on the ESP-IDF and the open-source OpenThread stack. It includes the necessary example projects and libraries to create both the OTBR firmware for the host and the RCP firmware for the radio co-processor.
- VSCode with ESP-IDF Extension 
  

------------------------------------------------------------------------------------------------------

📕 **YouTube Video Links**  

- In this tutorial we will see How to setup OTBR on ESP32 Boards - There are two methods, we have explained and demonstrated them in following videos  

▶️ OpenThread Border Router (OTBR) on ESP32 - Method (I)   - 🔗  https://youtu.be/dCaZpY5YMLk   
  
▶️ OpenThread Border Router (OTBR) on ESP32 - Method (II)   - 🔗  https://youtu.be/wcr7LpdBkp0   
  

-------------------------------------------------------------------------------------------------------
📒 **Important Links**  
 
🌐 What is OpenThread -  Docs - 🔗 https://github.com/openthread/openthread    
🌐 OpenThread Border Router - 🔗 https://openthread.io/guides/border-router   
📙 ESP32 OpenThread 🔗 https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/openthread.html  
🌐 ESP Thread Border Router SDK - 🔗 https://docs.espressif.com/projects/esp-thread-br/en/latest/  
🌐 ESP Thread Border Router SDK GitHub - 🔗 https://github.com/espressif/esp-thread-br    
🌐 OpenThread Border Router Example  - 🔗 https://github.com/espressif/esp-idf/tree/master/examples/openthread/ot_br    

------------------------------------------------------------------------------------------------------

📜 Source Code, Circuit Diagrams and Documentation : 

🌐 GitHub Repository - 🔗 https://github.com/make2explore/Open-Thread-Border-Router-On-ESP32   
  
🌐 Hackster Blog - 🔗 https://www.hackster.io/make2explore  
  
🌐 Instructable Blog - 🔗 https://www.instructables.com/make2explore  
  

------------------------------------------------------------------------------------------  

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg