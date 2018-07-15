
# Disable ASUS touchpad when typing

The touchpad is identified as a USB mouse. 
Disable-While-Typing feature in libinput is only available to touchpad (not mouse). 

## Prerequisites

```bash
sudo apt-get install python-pip
pip2 install python-libinput
```

## Setup

```bash
sudo cp 99-input.rules /etc/udev/rules.d/
sudo udevadm control --reload-rules && sudo udevadm trigger
```

# Rotate screen

The display is identified as 800x1280 (potrait) device. 

## Pre-boot

This configuration rotates pre-boot screen into landscape and skips GRUB bootloader. 

```bash
sudo cp grub /etc/default/
```

## Post-boot

```bash
xrandr -o left
```

