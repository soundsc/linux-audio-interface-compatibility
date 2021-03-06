# Linux Audio-Interface Compatibility

A list of audio interfaces that have been tested with Linux. Hopefully this
will help some people answer the question of "does it work on Linux" before
spending some money.

- ✓ [Allen & Heath XONE:K2](#allen--heath-xonek2)
- ✓ [Behringer UCA222](#behringer-uca222)
- ✓ [Behringer UFO202](#behringer-ufo202)
- ✓ [ESI UDJ6](#esi-udj6)
- ✓ [Native Instruments Audio 2](#native-instruments-audio-2)
- ✓ [Native Instruments Audio 4 DJ](#native-instruments-audio-4-dj)
- ✓ [Native Instruments Audio 6](#native-instruments-audio-6)
- ✓ [Native Instruments Audio 8 DJ](#native-instruments-audio-8-dj)
- ✓ [Rane SL-1](#rane-sl-1)
- ✖️ [Pioneer DJM-750MK2](#pioneer-djm-750mk2)

## Allen & Heath XONE:K2

- ✓ Working on Ubuntu 16.04

USB, 0 inputs, 4 outputs.

- http://www.allen-heath.com/ahproducts/xonek2/

## Behringer UCA222

- ✓ Working on Ubuntu 11.04

USB, 2 inputs, 2 outputs.

- http://www.behringer.com/EN/Products/UCA222.aspx

## Behringer UFO202

- ✓ Working on Ubuntu 11.04

USB, 2 inputs, 2 outputs.

- http://www.behringer.com/EN/Products/UFO202.aspx

## ESI UDJ6

- ✓ Working on Ubuntu 16.04

USB, 0 inputs, 6 outputs.

http://www.esi-audio.com/products/udj6/

The headphone output is incredibly loud. Turning down the volume with the ALSA
mixer lowers the volume but not the noise floor, so you get a very noisy
signal not really suited for use with headphones. Would work well for 6 hot
signals going into an external mixer or such.

## Native Instruments Audio 2

- ✓ Working on Ubuntu 16.04

USB, 0 inputs, 4 outputs.

- https://www.native-instruments.com/en/products/traktor/dj-audio-interfaces/traktor-audio-2/

## Native Instruments Audio 4 DJ

- ✓ Working on Ubuntu 16.04
- ✓ Working on Debian Jessie
- ✓ Working on Ubuntu 12.04
- ✓ Working on Ubuntu 10.10

USB, 4 inputs, 4 outputs. Toggleable phono preamps on all inputs.

Set inputs to Phono: `$ amixer -c [cardnumber] cset numid=1 0`

Set inputs to Line: `$ amixer -c [cardnumber] cset numid=1 1`

## Native Instruments Audio 6

- ✓ Working on Ubuntu 11.10

USB, 6 inputs, 6 outputs. Toggleable phono preamps on 4 inputs. Togglable
pass-thru on 4 inputs.

PASSTHRU on channel A: `$ amixer -c T6 cset numid=1 on/(off)`

PASSTHRU on channel B: `$ amixer -c T6 cset numid=2 on/(off)`

Switch PHONO/LINE on channel A: `$ amixer -c T6 cset numid=3 on/(off)`

Switch PHONO/LINE on channel B: `$ amixer -c T6 cset numid=4 on/(off)`

An `.asoundrc` file making this device present stereo pairs can be found here:
http://www.pogo.org.uk/~mark/linuxdj/t6.asoundrc

## Native Instruments Audio 8 DJ

- ✓ Working on Debian Jessie
- ✓ Working on Ubuntu 12.04
- ✓ Working on Ubuntu 10.10

USB, 8 inputs, 8 outputs. Toggleable phono preamps on 4 inputs.

Set inputs to Phono: `$ amixer -c [cardnumber] cset numid=1 1`

Set inputs to Line: `$ amixer -c [cardnumber] cset numid=1 0`

## Rane SL-1

- ✓ Working on Fedora ~2011. Unable to turn on the phono preamps.

USB, 4 inputs, 4 outputs. Toggable phono preamps on all 4 inputs.

- http://dj.rane.com/products/sl1-for-serato-scratch-live

## Pioneer DJM-750MK2

- ✖️ Not working on Ubuntu 16.04. Nothing appears to happen when plugged.

USB, 10 inputs, 10 output (?). Toggleable phono preamps on 4 inputs.

- https://www.pioneerdj.com/en-gb/product/mixer/djm-750mk2/black/overview/
