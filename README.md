# crkbd-vial-firmware-keymap

- Install QMK-MSYS and qmk\_toolbox.
- Clone [vial-qmk](https://github.com/vial-kb/vial-qmk)
- Enter in the repository and prepare qmk: `cd vial-qmk && qmk setup`
- Compile the vial keymap: `qmk compile -kb crkbd -km vial`. The file `crkbd_rev1_vial.hex` is generated inside the `vial-qmk` folder.
    If you are using an arduino micro you may need to add `#define SPLIT_USB_DETECT` to the file `keyboards/crkbd/keymaps/vial/config.h`. You might also need to enable the OLEDs in the file `keyboards/crkbd/keymaps/vial/rules.mk` by setting `OLED_ENABLE` to `yes`.
- You can now flash the hex file using qmk\_toolbox.
