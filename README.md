```
# /etc/udev/rules.d/99-input.rules
KERNEL=="event*", MODE="0666"
```

```bash
sudo udevadm control --reload-rules && sudo udevadm trigger
```
