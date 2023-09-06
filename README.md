![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg)

# What is Tiny Tapeout?

TinyTapeout is an educational project that aims to make it easier and cheaper than ever to get your digital designs manufactured on a real chip!

Go to https://tinytapeout.com for instructions!

![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg)

# What is Tiny Tapeout?

TinyTapeout is an educational project that aims to make it easier and cheaper than ever to get your digital designs manufactured on a real chip!

## Project Randomizer and Status Checker
link github: https://github.com/karla-gabrielly/tt04-Randomizer-and-status-checker

language: "wokwi"

wokwi_id: 375075618467202049

## How does it works?
General Description: The circuit is a random number generator, that will turn on a random LED between LED 1 and LED 4. Then, the player should press the button with the number corresponding to the LED that is on, and the circuit will say if it is the RIGHT or WRONG button. The button 0 will make the circuit restart, generating another random number.

Blocks Description: When ON, the circuit will run a 4 bit counter, that will oscilate between 0 and 3 (binary). When the 0 button receives an input, the randomizer will select the number out of the counter, and send it to decoder, that will turn on one of the LEDs.

Now, the user have to press a button between 1 and 4, that correspondes to the LED that is on. This signal is sent to the comparator, that will cross the information with the LEDs that is on, and will sign if was pushed the right or the wrong button with the Right or Wrong LEDs.
As the goal is to use "no hold" buttons, the signal will be sent to the state maintainer, that will keep it in high level, so the right/wrong LEDs keep on. When the button 0 is pressed again, the state maintainer will reset it output.

## How to test it?
In the inputs, the user will need to connect 5 momentary switch labeled from "Button 0" to "Button 4." The clock signal considered in CLK is 64 Hz, but any value above 20 Hz will work as expected. 
On the ON/OFF input, a switch should be connected, or it can be driven directly to a high logic level.
On the outputs, 6 LEDs should be connected.
To start, the first step is to turn the switch to ON/OFF, and then press BUTTON 0.
One of the four LEDs will light up.The user should press the button corresponding to the LED that is on. If the correct button is pressed, the RIGHT LED will light up; if another button is pressed, the WRONG LED will light up.

## Picture:
<img src=Wokwi-circuit.png>


## Inputs:

CLK

ON/OFF

Botão 0

Botão 1

Botão 2

Botão 3

Botão 4

Seletor


## Outputs:

Led 1

Led 2

Led 3

Led 4

Right

Wrong

none

none

## Resources

- [FAQ](https://tinytapeout.com/faq/)
- [Digital design lessons](https://tinytapeout.com/digital_design/)
- [Learn how semiconductors work](https://tinytapeout.com/siliwiz/)
- [Join the community](https://discord.gg/rPK2nSjxy8)

## What next?

- Submit your design to the next shuttle [on the website](https://tinytapeout.com/#submit-your-design), the closing date is 8th September.
- Share your GDS on Twitter, tag it [#tinytapeout](https://twitter.com/hashtag/tinytapeout?src=hashtag_click) and [link me](https://twitter.com/matthewvenn)!
