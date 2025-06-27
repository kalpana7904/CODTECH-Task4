## Name:P.kalpana
## Company:CODETECH IT SOLUTIONS
## CT06DF1896
## Domain:Embedded Systems
## Duration:May to july
## Mentor:Neela santhosh kumar 
### *Overview of Speech Recognition System for Command-Based Device Control Using an Embedded Board*  

This project implements a *voice-controlled system* that recognizes spoken commands and triggers actions on connected devices (e.g., lights, fans, motors) using an *embedded board* (e.g., ESP32, Raspberry Pi). The system operates *offline* (no cloud dependency) and is optimized for low-power, real-time performance.  

---

## *1. Core Components*  

### *A. Hardware*  
1. *Microcontroller* (Choose one):  
   - *ESP32* (Best for low-power, TinyML-based edge computing).  
   - *Raspberry Pi* (More powerful, supports Python/cloud APIs).  
2. *Microphone* (Input):  
   - *Digital (I2S)*: INMP441 (better noise rejection).  
   - *Analog*: MAX9814 (requires ADC).  
3. *Output Devices*:  
   - LEDs (for testing).  
   - Relays (to control AC appliances).  
   - Servo motors (for physical movements).  

### *B. Software*  
- *Speech Recognition Engine*:  
  - *Offline*:  
    - *TinyML (TensorFlow Lite)* → For ESP32.  
    - *PocketSphinx* → For Raspberry Pi.  
  - *Online (if using RPi + Wi-Fi)*:  
    - Google Speech-to-Text API.  
- *Firmware*:  
  - *C++ (Arduino IDE)* → For ESP32.  
  - *Python* → For Raspberry Pi.  

---

## *2. How It Works*  

### *Step 1: Voice Input*  
- A microphone captures the user’s voice command.  
- *Sampling Rate: Typically **16 kHz* (for clear speech).  

### *Step 2: Audio Preprocessing*  
- *Noise Reduction*: Filters background noise (if using a digital mic).  
- *Feature Extraction: Converts raw audio into **MFCCs* (Mel-Frequency Cepstral Coefficients), a compact representation for speech recognition.  

### *Step 3: Command Detection*  
- A *pre-trained ML model* (TinyML on ESP32 or PocketSphinx on RPi) classifies the spoken phrase.  
- Example commands:  
  - *"Turn on light"* → GPIO activates LED.  
  - *"Fan speed high"* → PWM increases motor speed.
  - ### *Step 4: Device Control*  
- The microcontroller triggers *GPIO pins* to:  
  - Turn relays on/off.  
  - Adjust motor speed via PWM.  
  - Display feedback on an OLED screen.
  - ## *4. Applications*  
✅ *Smart Home Automation* – Voice-controlled lights, fans.  
✅ *Industrial IoT* – Hands-free machine control.  
✅ *Accessibility Devices* – Voice-operated wheelchairs.  
✅ *DIY Robotics* – Voice commands for robot movements.  
## *5. Challenges & Solutions*  

| *Challenge*               | *Solution*                          |  
|-----------------------------|---------------------------------------|  
| Background noise            | Use digital mics (INMP441) + noise filters |  
| Limited ESP32 memory        | Optimize TensorFlow Lite model        |  
| Accent/voice variations     | Train model with diverse samples      |  

---

## *6. Future Enhancements*  
🔹 *Wake Word Detection* (e.g., "Hey Device, turn on light").  
🔹 *Multi-language Support* (train model in Spanish, Hindi, etc.).  
🔹 *Wireless Control* (ESP32 sends commands via Wi-Fi/BLE).  

## DELIVERABLE:
# System design :![WhatsApp Image 2025-06-27 at 09 44 32_73a53a5d](https://github.com/user-attachments/assets/a38e4121-d58c-46e4-9d03-1962ce00f93a)
# Working demo: "C:\Users\kalpa\OneDrive\Documents\speech recognition system.mp4"




 

