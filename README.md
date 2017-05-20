# Description
A minimal example to use Real Time Transfer (RTT) for debugging on a Nordic Semiconductor nRF52 SDK.

The code and Makefile are based on the "blinky" example project from SDK 11 by Nordic Semiconductor.

# Running
## Prerequisites
Install Nordic SDK11 and JLink debugging tools. You also need an [RTT implementation](http://download.segger.com/J-Link/RTT/RTT_Implementation_141217.zip) that will run on your microcontroller. Connect a nRF52 dev kit to your USB port. 

## Configure the Makefile
Set ``SDK_DIR`` to the path to the Nordic SDK and ``RTT_DIR`` to the SEGGER RTT dir in the Makefile.

## Build
``make``

## Flash
``make flash``

## Run RTT server
Open a terminal and run:

``JLinkExe -device NRF52 -speed 4000 -if SWD``

type ``connect``, then hit enter. Alternatively, add the flag ``-AutoConnect`` to the JLinkExe command.

## Connect to RTT
Open a new terminal, then run ``JLinkRTTClient``.
