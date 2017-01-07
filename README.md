# max-power: Multi ATX Cross Power

This is just a dumb PCB that I designed to end with the big mess of wall adapters I have under my TV, powering two RaspberryPi boards, several hard disks, routers, a USB hub, an HDMI to optical splitter, and maybe something more I'm missing right now. The board provides the following outputs:

* 2x5V standby (USB-A, always ON)
* 6x5V (USB-A)
* 6x12V (Terminal blocks)
* 4x3.3V (Terminal blocks)

It also features a power button and a power LED.

## Usage

The board must be connected at least to an ATX power source (I use a very old 300W one) and to a Raspberry Pi (that will be always powered, I connect the one I use as home server). This RPi is connected to an internal ATX +5V_SB rail, so as long as the ATX PS is powered, so will be this RPi. To power ON/OFF all the power outputs (other than the +5V_SB ones), a small program on the RPi monitors:
* The power button on the board; and
* The network for specially crafted packets.

This way the PS can be switched ON/OFF either by pressing the power button, or by using an application (e.g. on a smartphone) to send power ON/OFF commands.

## Licenses

Hardware designs under this repository are licensed under the CERN OHL 1.2 license.

Software sources under this repository are licensed under the GPL v3+ license.

