                                         Project-C4
                                          By Koray 
![image alt](https://github.com/koray9012/Project-C4/blob/main/15517.jpg?raw=true)
An interactive, DIY Counter-Strike 2 inspired bomb prop built for airsoft games and tabletop fun. Powered by an Arduino Uno, featuring dynamic countdown audio, interactive defusal guessing mechanics, and a 16x2 LCD interface.

## Disclaimer: This project is purely an electronic game prop / toy intended for airsoft recreation and custom gaming setups. It contains no hazardous or explosive materials.

## Key Info
  
Hardware Core:
 
 • Built on an Arduino Uno powered by a 9V battery with an integrated ON/OFF switch.
 
Display & Keypad:

 • Features a 16x2 I2C LCD for real-time status updates and a 4x3 matrix keypad for code entry.

Audio & Visuals:

 • Driven by a passive piezo buzzer (with custom pitch settings for maximum volume) and an LED indicator. 

## Key Features

CS2 Authentic Gameplay:

 • Uses the iconic 7355608 bomb code for arming and defusal.

Trial-and-Error Defusal:

 • Automatically generates a random secret digit (0-9) on arming. Defusers must enter the code plus the correct extra digit (7355608X) before time runs out.

Exponential Countdown Pinging:

 • Features a custom CS2 audio formula where beep frequency speeds up exponentially as the 45-second timer gets closer to 0.

Anti-Spam Delay:

 • Includes a non-blocking 0.7-second cooldown on wrong guesses (INCORRECT CODE!) to prevent blind button mashing while keeping the live timer visible.

Hardware Noise Filtered:

 • Programmed with keypad debounce protection to prevent ghost keypresses caused by buzzer power draws.

System Soft-Reset:

 • Allows players to hold the * key for 4 seconds at the end of a round to immediately reset the prop for the next match.

 ## How to use:

Arming the Bomb (T Side):

 1. Power on the device using the toggle switch on the side.

 2. Enter the arming password 7355608 on the keypad.

 3. Press # to lock in the code and start the 45-second countdown.
(Press * at any time before hitting # if you make a mistake and need to clear your input.)

Defusing the Bomb (CT Side):

 1. Press # on the keypad while the bomb is active to open the defusal prompt.

 2. Key in the base password 7355608 followed by your guess for the secret 8th digit (0–9).

 3. The bomb will auto-check as soon as the 8th digit is pressed:

    • If correct: The LCD displays BOMB DEFUSED and plays the CT victory chime.

    • If incorrect: The screen flashes INCORRECT CODE! for 0.7 seconds with an error buzz, then automatically clears your entry so you can guess the next digit.

Round End & Resetting:

  • If the timer hits 0.0s, the bomb detonates, displaying BOOM! alongside explosion sound effects.

  • After a defusal or explosion, press and hold the * key for 4 seconds to reset the prop for the next round.

## Why i made it:

 • Level Up Airsoft Matches: Standard airsoft games can get repetitive with simple flag-capturing; adding a physical CS2 bomb prop brings intense objective-based gameplay and real time pressure to every round.

 • Tackle a Coding Challenge: The original setup was too basic (just holding down # to defuse), so I wanted to re-engineer the software to create a custom trial-and-error defusal mechanic and clean up state management.

 • Bring CS2 to Life: As a fan of Counter-Strike, replicating the authentic arming sequence, explosive exponential beep timing, and high-stakes feel on real hardware was a fun DIY project.

 • Budget-Friendly Engineering: Built entirely out of spare Arduino starter kit components and a simple cardboard box to prove that engaging game props don't require expensive commercial gear.

 ## Wiring & Connections:

 Below is a visual schematic of the wiring for the Project-C4

![image alt](https://github.com/koray9012/Project-C4/blob/main/%D0%95%D0%BA%D1%80%D0%B0%D0%BD%D0%BD%D0%B0%20%D1%81%D0%BD%D0%B8%D0%BC%D0%BA%D0%B0%202026-08-19%20182526.png?raw=true)

### Pinout breakdown:

| Arduino Pin | Component | Connected Pin / Note |
| :--- | :--- | :--- |
| **SDA/A4** | LCD Display Driver | SDA |
| **SCL/A5** | LCD Display Driver | SCL |
| **Pin 9** | Button Matrix | Row 1 (1,2,3) |
| **Pin 8** | Button Matrix | Row 2 (4,5,6) |
| **Pin 7** | Button Matrix | Row 3 (7,8,9) |
| **Pin 6** | Button Matrix | Row 4 (*,0,#) |
| **Pin 5** | Button Matrix | Col 1 (1,4,7,*) |
| **Pin 4** | Button Matrix | Col 2 (2,5,8,0) |
| **Pin 3** | Button Matrix | Col 3 (3,6,9,#) |
| **9V Battery +** | switch | Pin 1 |
| **Switch Pin 2** | Arduino | 12V jack |
| **9V Battery -** | Arduino | 12V jack |
| **VCC** | LCD Display Driver | 5V |
| **GND** | LCD Display Driver | GND |
| **Pin 10** | Buzzer | + (with 110ohm resistor) |
| **Gnd** | Buzzer | GND |

## Code:
The code can be found in repo: Project-C4 code

## Bill Of Materials:

| Item | Quantity | Price (USD) | Link |
| :--- | :--- | :--- | :--- |
| Arduino Uno R3 | 1 | 4.44 USD | https://elimex.bg/product/71201-kit-k2014-razvoyna-platka-s-atmega328p-smd-usb-b |
| LCD Display | 1 | 22.02 USD | https://elimex.bg/product/94768-lcd-rc1602e-biy-esx |
| Buzzer | 1 | 0.30 USD | https://elimex.bg/product/81601-zumer-0152-12v-pasiven |
| 4x3 Button Matrix | 1 | 2.32 USD | https://elimex.bg/product/74899-kit-k2143-matrichna-klaviatura-4h4-s-16-butona-panelen-tip (my store has stopped selling the 4x3 so im gonna put the 4x4 here) | 
| 9V battery| 1 | 2.32 USD | https://elimex.bg/product/93070-bateriq-6lp3146-varta-energy |
| 9V battery Jack| 1 | 0.54 USD | https://elimex.bg/product/77718-f172b-battery-clip-9v-to-dc-plug-2-1x5-5mm |
| Switch| 1 | 0.36 USD | https://elimex.bg/product/44024-switch-smrs101-1-black |




 

  

    

 




 
