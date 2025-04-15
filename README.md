
# Biometric Electronic Voting Machine (EVM) using Arduino

This project demonstrates a *basic Electronic Voting Machine (EVM)* that uses *fingerprint biometric authentication* to ensure secure, one-person-one-vote elections. It’s built using an *Arduino UNO, an **R305 fingerprint sensor*, and components like buttons, LEDs, LCD, and EEPROM.

## Features

- Fingerprint-based voter authentication
- Supports voting for 3 candidates
- Prevents duplicate voting (EEPROM used to track voted users)
- Displays real-time results on a 16x2 LCD
- Uses buzzer and LEDs for user feedback
- Offline system – no network dependency

## Hardware Requirements

- Arduino UNO
- R305 Fingerprint Sensor
- LCD 16x2 Display
- Push Buttons (Match, Enroll, Result, Candidate 1/2/3)
- Green and Yellow LEDs
- Buzzer
- EEPROM (built-in)
- Breadboard, jumper wires, power supply

## Wiring Overview

| Component         | Arduino Pin     |
|------------------|-----------------|
| R305 TX/RX       | 2 and 3         |
| LCD              | Pins 8–13       |
| Enroll Button    | A3              |
| Match Button     | A4              |
| Candidate Buttons| 4, 5, A1        |
| Result Button    | A0              |
| Green LED        | 6               |
| Yellow LED       | 7               |
| Buzzer           | A5              |

## How It Works

1. *Enroll Voter*: Admin presses Enroll button. Voter scans their fingerprint (twice).
2. *Authenticate & Vote*: Voter presses Match button and scans fingerprint.
3. *Vote Selection*: If verified and not voted, voter selects a candidate.
4. *Result Display*: Press the Result button to show vote counts and winner.

## Code Structure

- setup(): Initializes hardware and resets data.
- loop(): Waits for button presses to trigger actions.
- enrollUser(): Captures and stores fingerprints.
- authenticateVoter(): Verifies voter and processes the vote.
- displayResults(): Shows voting summary and winner.

## Screenshots / Demo

(You can include images of the setup and LCD display outputs)

## License

This project is open-source for educational purposes.

---
