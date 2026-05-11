# uDOS v1.0

A DOS-like shell and RAM filesystem for Arduino UNO R3. Write files, control GPIO pins, read sensors, and run simple scripts all from the serial terminal.


# Commands (26):

- `dir`
- `cd`
- `path`
- `md`
- `mkf`
- `type`
- `echo`
- `del`
- `attrib`
- `pinmode`
- `write`
- `read`
- `gpio`
- `pwm`
- `bat`
- `uptime`
- `ver`
- `syslog`
- `mem`
- `whoami`
- `cls`
- `reboot`
- `search`
- `doskey`
- `slots`

## How It Works

The code manages a virtual filesystem stored in RAM:
- Maximum 10 files/directories
- Max 32 bytes per file content
- 12 character names
- Automatic `/home` directory created on boot
- `COM2`, `COM3`, `COM4` are special files for GPIO

GPIO control uses standard Arduino functions: `pinMode()`, `digitalWrite()`, `digitalRead()`, and `analogWrite()`.

Input is buffered from the serial connection and parsed line-by-line. Commands are case-insensitive.

## Planned Features

- EEPROM support
- I2C interface
- Date cmd
- neofetch cmd

## License

BSD3 - Original by [Arc1011](https://github.com/Arc1011/KernelUNO)

