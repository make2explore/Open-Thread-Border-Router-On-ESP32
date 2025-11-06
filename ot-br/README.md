### OpenThread Border Router on ESP32

Building an OpenThread Border Router (OTBR) on an ESP32 typically requires a two-chip architecture consisting of a Wi-Fi capable ESP32 host processor and an ESP32-H2 radio co-processor (RCP) with an IEEE 802.15.4 radio for Thread networking. Software requirements include Espressif's ESP-IDF framework and their ESP Thread Border Router SDK to build and flash the necessary RCP and border router firmware.  
  
A basic example for setting up an OTBR on an ESP32 using a dual-chip architecture is available in the [`espressif/esp-idf/tree/master/examples/openthread/ot_br`](https://github.com/espressif/esp-idf/tree/master/examples/openthread/ot_br) GitHub repository.  
  
For more details, visit the official Espressif OpenThread guide: [docs.espressif.com](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/openthread.html).
  
## Commands to test the OpenThread Border Router on ESP32  
  
- To create and Test the Thread network, we have shared the commands we used in the video - you can refer them from following [guide](https://github.com/make2explore/Open-Thread-Border-Router-On-ESP32/tree/main/Testing-THREAD-setup)  
  
🔗 `https://github.com/make2explore/Open-Thread-Border-Router-On-ESP32/tree/main/Testing-THREAD-setup`   