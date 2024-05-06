# crkbd-vial-firmware-keymap

- Install QMK-MSYS and qmk\_toolbox.
- Clone [vial-qmk](https://github.com/vial-kb/vial-qmk)
- Enter in the repository and prepare qmk: `cd vial-qmk && qmk setup`
- Compile the vial keymap: `qmk compile -kb crkbd -km vial`. The file `crkbd_rev1_vial.hex` is generated inside the `vial-qmk` folder.
    If you are using an arduino micro you may need to add `#define SPLIT_USB_DETECT` to the file `keyboards/crkbd/keymaps/vial/config.h`. You might also need to enable the OLEDs in the file `keyboards/crkbd/keymaps/vial/rules.mk` by setting `OLED_ENABLE` to `yes`.
- You can now flash the hex file using qmk\_toolbox.

When you turn on your computer it might happen that your keyboard freezes, remember to define the following in your config.h:
```c
#define SPLIT_USB_DETECT
#define SPLIT_USB_TIMEOUT 2000
#define SPLIT_USB_TIMEOUT_POLL 10
#define SPLIT_WATCHDOG_ENABLE
#define SPLIT_WATCHDOG_TIMEOUT 3000
```
