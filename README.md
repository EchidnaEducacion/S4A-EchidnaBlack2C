# S4A EchidnaBlack2C for Snap!

This repository contains a Snap! project/library that adds a custom **`S4A Connector`** block category for the **EchidnaBlack2C** board.

The library is designed to connect Snap! with the board through **SA5 Firmata** and expose both:

- generic board I/O blocks
- board-specific blocks for the EchidnaBlack2C hardware

Snap! is a visual programming language developed by UC Berkeley:
<https://snap.berkeley.edu/>

Echidna project website:
<https://echidna.es>

Official manual:
<https://snap.berkeley.edu/snap/help/SnapManual.pdf>

## Repository contents

- `S4A-EchidnaBlack2C.xml`: main Snap! library/project with the custom blocks.
- `Test-EchidnaBlocks-Snap.xml`: example/test project that exercises the available blocks.

## What this library adds

The XML project defines a custom **`S4A Connector`** palette with blocks for:

- connection status (`board connected?`)
- digital output and input
- analog reading
- PWM output
- servo control
- I2C read/write/send operations
- tone, pulse out, pulse in, and ping-style sensor operations
- Nunchuk and DHT11 helper blocks

It also includes higher-level blocks tailored to the **EchidnaBlack2C** board, such as:

- onboard LEDs and RGB LED control
- buzzer control
- servo outputs on predefined pins
- board buttons
- MkMk touch/input checks
- joystick reading
- accelerometer reading
- light sensor reading
- temperature reading
- microphone reading
- generic analog input reading on supported pins

## Requirements

To use this library you need:

- Snap! compatible with importing/opening project XML files
- Google Chrome or Chromium, so Snap! can access the board over USB
- an **EchidnaBlack2C** board
- the board firmware/bridge expected by the project: **SA5 Firmata**
- access to the `s4aConn` connector module referenced by the project

The project XML points to:

- `libraries/s4aConn/init.js`

So the Snap! environment you use must provide that connector support.

## How to use it

1. Open Snap!.
2. Load or import `S4A-EchidnaBlack2C.xml`.
3. Use Chrome or Chromium, since the USB connection requires a browser that supports it.
4. Connect the EchidnaBlack2C board with the expected SA5 Firmata setup.
5. Click the `Connect` button in Snap! to establish the USB connection.
6. Look for the **`S4A Connector`** category in the palette.
7. Use `board connected ?` to verify communication before running hardware scripts.

If you want a ready-made example, open `Test-EchidnaBlocks-Snap.xml`.

## Notes

This repository stores the library as standard Snap! project XML, which makes it easy to:

- share with educators and students
- import into Snap! projects
- inspect or extend the block definitions manually if needed

The included test project is useful as a quick validation script for the board sensors and actuators.
