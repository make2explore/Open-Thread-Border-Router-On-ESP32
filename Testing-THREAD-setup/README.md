# Testing a Thread Network with OTBR and ESP32 Devices

This guide outlines the steps to set up and test a Thread network, using a ESP32-based OpenThread Border Router (OTBR), ESP32-C6 programmed as Thread end devices (Thread-Matter Light Application), and Amazon Echo as a smart home controller.

---

## 🧠 Overview

- OTBR is already set up on the ESP32 boards.
- We will create and configure a new Thread network.
- ESP32-C6 will act as Thread Light devices.
- The Thread network will be tested and controlled using Amazon Echo.

---

## 🧪 Create and Start a Thread Network

### 🔧 In Serial terminal of ESP32-C3 - (ot_br) Launch OpenThread CLI

```bash
sudo ot-ctl
```

### 🆕 Create a New Network Dataset

```bash
dataset init new
```

### 🔍 View Dataset Parameters

```bash
dataset
```

### ✏️ Customize Network Settings

You can change parameters such as the channel number or network key:

```bash
dataset networkkey 1626472a4b630f140e20b58998fe88a7
dataset channel 11
```

### ✅ Commit the Dataset

```bash
dataset commit active
```

### 🚀 Start the Thread Network

```bash
thread start
```

### 🔍 Verify Network Status

```bash
netdata show
```

---

## 💡 Notes

- Ensure that your ESP32-C6 devices is programmed as Thread End Devices and have the credentials to join this network.
- The Amazon Echo must support Thread and be connected to the same Thread network to control these lights.
- All devices should reside within the same 802.15.4 radio range.

---