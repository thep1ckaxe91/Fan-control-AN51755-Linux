# Fan-control-AN51755-Linux
A bash-script that write directly to EC registers to control the modes and speed of Acer Nitro 5 model 51755 specifically

You may try this in others devices to see if it works, only if the address were match thou, and also the key values at 0x03 to unlock manual control mode

changing 0x21 to 02 make the fan on the left 
0x36 and 0x3A is the place to save the fan speed for custom mode of the left fan and the right fan

Only tested on AN51755, use at your own risk

## How to Use

Run the script as root or with `sudo`. The commands are organized to mirror the original Nitro Sense GUI sections.

### 1. Fan Control
| Command | Action | Description |
| :--- | :--- | :--- |
| `sudo nitro-sense auto` | **Auto** | Standard automatic fan control. |
| `sudo nitro-sense max` | **Max** | Forces both fans to 100% speed. |
| `sudo nitro-sense custom <cpu_%> <gpu_%>` | **Custom** | Manually set fan speeds (0-100). |

### 2. Mode (Fan Curves)
| Command | Action | Description |
| :--- | :--- | :--- |
| `sudo nitro-sense mode quiet` | **Quiet** | Minimizes fan noise. |
| `sudo nitro-sense mode default` | **Default** | Balanced thermal profile. |
| `sudo nitro-sense mode performance` | **Performance** | Aggressive cooling for gaming. |

### Examples
```bash
# Set fans to Max speed
sudo nitro-sense max

# Set CPU fan to 80% and GPU fan to 50%
sudo nitro-sense custom 80 50

# Switch to Performance mode
sudo nitro-sense mode performance
```

## Install

Just put it in any path in env,ex: /usr/bin/

## Future

Looking foward to build a gui for this with python
