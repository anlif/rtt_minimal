# Description
A minimal example to use Real Time Transfer (RTT) for debugging on a Nordic Semiconductor nRF52 SDK.

# Running
## Prerequisites
Install Nordic SDK11 and JLink debugging tools. Connect a nRF52 dev kit to your USB port. Set proper SDK and RTT paths in the Makefile.

## Build
``make``

## Flash
``make flash``

## Run RTT server
Open a terminal and run:

``JLinkExe -device NRF52 -speed 4000 -if SWD``

type ``connect``, then hit enter

## Connect to RTT
Open a new terminal, then run ``JLinkRTTClient``.
