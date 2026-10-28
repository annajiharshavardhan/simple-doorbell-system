# Simple Doorbell System (Arduino Uno)

A push button that activates a buzzer. The buzzer sounds only while the
button is held and stops immediately when it is released.

## Links
- Tinkercad simulation: https://www.tinkercad.com/things/kYsA0pk0YpZ-simple-doorbell-system?sharecode=7JA-lE_0_Hv2IChPyYTgRyouPANQ5awitfgz5cKS-as
- Full report (Google Docs): https://docs.google.com/document/d/1O_2uv7FNUpLuyT4rg2y50OuCBIz1BiZKulNCHVYqbCE/edit?usp=sharing

## Components
Arduino Uno, push button, piezo buzzer, breadboard, jumper wires

## Connections
| Part | Pin | Arduino |
|---|---|---|
| Push button | leg 1 | D2 |
| Push button | opposite leg | GND |
| Buzzer | + | D8 |
| Buzzer | - | GND |

## How it works
The button uses the internal pull-up (`INPUT_PULLUP`), so D2 reads LOW
when pressed. The code plays a 1 kHz tone on D8 while D2 is LOW and
calls `noTone()` when it is released.

## Code
See `doorbell.ino`.

## Output
![Circuit] <img width="835" height="679" alt="image" src="https://github.com/user-attachments/assets/1b2fba60-ab72-4462-b4a8-eeebc2b36b69" />

![Pressed] <img width="866" height="683" alt="image" src="https://github.com/user-attachments/assets/2a0c07c5-46ea-4138-ad8f-33165e2beb9b" />

![Released] <img width="938" height="670" alt="image" src="https://github.com/user-attachments/assets/0a9cf938-c253-4428-98b8-b8c4ea5e0b96" />
