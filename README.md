# radio-on-a-card

## Introduction

This repo is the place I will store all the thoughts/progress/details for the Radio Coprocessor project.

The high level idea is to build a PCIe card that has a powerful HF-capable SDR on it, which you can connect to a (Linux) computer as an expansion card. It will show up as two devices:

- A sound card
- A PCIe device with an associated device driver (source code will go here)

The sound card exists to provide audio input to the radio and return audio output. The PCIe character device exists to send command instructions to the SDR, such as changing power settings, tuning the antenna, and changing the VFO setting.

Eventually, I plan to implement a user-space driver which will plug into some open source SDR software so people get the normal SDR experience they expect.

## Contents

This repo (will) contain three subdirectories:

- `architecture`, which will have informational documents about how the project is put together
- `hardware`, where board layout and list of components will live
- `software`, where the device drivers and software we use to run the SDR will live.
