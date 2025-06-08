# Fan-control-AN51755-Linux
A bash-script that write directly to EC registers to control the modes and speed of Acer Nitro 5 model 51755 specifically

You may try this in others devices to see if it works, only if the address were match thou, and also the key values at 0x03 to unlock manual control mode

changing 0x21 to 02 make the fan on the left 
0x36 and 0x3A is the place to save the fan speed for custom mode of the left fan and the right fan

Only tested on AN51755, use at your own risk

## How to use

**You may see how to use in the script itself**

## Install

Just put it in any path in env,ex: /usr/bin/

## Future

Looking foward to build a gui for this with python
