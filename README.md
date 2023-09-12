# Codes for SMSL IR Remotes

Read using an ESP32 dev board and [Arduino-IRremote library](https://github.com/Arduino-IRremote/Arduino-IRremote) (ReceiveDump example).

## Unknown model

This type was supplied with SMSL AO200 amplifier, it does not have any visibel model number:

![image](https://github.com/raintonr/SMSL-Remote-Codes/assets/3794098/c83fdcfe-ebef-4920-ace2-eae02a536dcf)

The A/B/C buttons do not emmit a signal, and are used to change the address of other buttons.

After A address is 0x3412.
After B address is 0x3512.
After C address is 0x3612.

Commands are identical in each mode (just the address changes):

| Button | Command |
| ------ | ------- |
| Power  | 0x1     |
| Mute   | 0x9     |
| Up     | 0x2     |
| Down   | 0x6     |
| Left   | 0x3     |
| Right  | 0x5     |
| OK     | 0x4     |
| Input  | 0x7     |
| FN     | 0x8     |

## RC-8C

This type was supplied with SMSL DO100 DAC and is labeled RC-8C:

![image](https://github.com/raintonr/SMSL-Remote-Codes/assets/3794098/381b8682-d52a-43b3-b0c6-c9ca292057f6)
