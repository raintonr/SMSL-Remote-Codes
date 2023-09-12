# Codes for SMSL IR Remotes

Read using an ESP32 dev board and [Arduino-IRremote library](https://github.com/Arduino-IRremote/Arduino-IRremote) (ReceiveDump example).

Codes can be sent with this library using `sendNEC`:

```
IrSender.sendNEC(address, command, numberOfRepeats);
```

## Unknown model

This type was supplied with SMSL AO200 amplifier, it does not have any visible model number:

![SMSL Unknown (AO200) Remote](SMSL%20Unknown%20(AO200)%20Remote.png)

The A/B/C buttons do not emmit a signal and are used to change the address of other buttons.

- After A address is 0x3412.
- After B address is 0x3512.
- After C address is 0x3612.

Commands are identical in each mode:

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

![SMSL RC-8C Remote](SMSL%20RC-8C%20Remote.png)

Commands are transmitted with address 0x3612.

| Button | Command |
| ------ | ------- |
| Power  | 0x1     |
| Up     | 0x2     |
| Down   | 0x6     |
| Left   | 0x3     |
| Right  | 0x5     |
| Centre | 0x4     |
| Input  | 0x7     |
| FN     | 0x8     |
| Mute   | 0x9     |
| +      | 0xA     |
| -      | 0xB     |
