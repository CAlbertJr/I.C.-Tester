
## Arduino Mega IC Tester 
An automated, hardware-based integrated circuit (IC) tester built using the Arduino Mega 2560. This project allows you to quickly verify the functionality of various digital logic gates, multiplexers, flip-flops, and operational amplifiers by running automated truth-table and parametric tests. 
## 🚀 Features

* Broad IC Support: Tests 74xx series TTL, 40xx series CMOS, and various common ICs.
* Auto-Detection: Automatically identifies unknown ICs by scanning pin configurations.
* Massive I/O Capacity: Utilizes the Arduino Mega's 54 digital pins to test up to 24-pin ICs without external multiplexers.
* User Interface: Features an optional 16x2 LCD screen/OLED display and a 4x4 matrix keypad for standalone operation.
* Serial Monitoring: Detailed pass/fail reports sent directly to your PC via USB Serial. 

## 🛠️ Hardware Requirements

* Arduino Mega 2560
* 16-pin or 24-pin Zero Insertion Force (ZIF) Socket
* 16x2 I2C LCD Display (Optional)
* 4x4 Matrix Keypad (Optional)
* 220-ohm current limiting resistors
* Breadboard and jumper wires 

## 📐 Pin Mapping

| IC ZIF Pin | Arduino Mega Pin | Function |
|---|---|---|
| Pin 1 | Digital Pin 22 | Configurable I/O |
| Pin 2 | Digital Pin 23 | Configurable I/O |
| VCC | 5V | Power Supply |
| GND | GND | Ground |

(Note: Modify the config.h file to match your exact wiring layout.)
## 💻 Software Setup

   1. Clone the repository:
   
   git clone https://github.com
   
   2. Open the project:
   Launch the Arduino IDE and open arduino-mega-ic-tester.ino.
   3. Install Dependencies:
   Install the following libraries via the Arduino Library Manager:
   * LiquidCrystal_I2C (if using an LCD)
      * Keypad (if using a physical keypad)
   4. Upload:
   Select Arduino Mega 2560 under Tools -> Board and upload the sketch. 

## 🔍 How It Works
The firmware configures the Arduino pins dynamically as inputs or outputs based on the selected IC database profile. It applies a series of binary inputs (truth tables) to the IC input pins and reads the resulting outputs. If the outputs match the expected logic states, the IC passes; otherwise, it fails and flags the faulty pins. 
## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request to add new IC definitions to the database file (ic_database.h).
