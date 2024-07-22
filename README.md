# What?
A simple Magisk module for Android which remaps physical hardware keys to any of Android's [virtual software keycodes](https://source.android.com/devices/input/key-character-map-files). For example, remapping your physical *VOLUME_UP* key to *KEYCODE_POWER* (power button) because your Xiomi device jsut started holding down the power button on its own, causing bootloops (See https://redd.it/17h989a)

By default, the following keys are remapped:
* VOLUME_UP --> KEYCODE_POWER
* Normal codes for POWER button are commented out.

# Why?
See reddit post.

# How?
This is accomplished by ~~modifying~~ `Generic.kl` in `/system/usr/keylayout/`. Thanks to Magisk, we can inject these files systemlessly without modifying the root filesystem; the net effect is the same.

# Help?!
This module does not include any options for customization. However, doing so is trivial. If you wish to add or modify any key bindings, you can download the [latest release](https://github.com/Jefferderp/Magisk-KeyboardRemaps/releases/latest), unpack the zip file, and add or modify files as desired. The existing file contains my customizations, which are clearly notated. Refer to [this page](https://developer.android.com/reference/android/view/KeyEvent) for a list of valid keycodes. Once finished, re-zip the module and install via Magisk.

See [Issue #3](https://github.com/Jefferderp/Magisk-KeyboardRemaps/issues/3) if you get stuck.

# I said help!?
While I appreciate your interest in this module, I'm not offering support unless you have a specific question. Every Android device is different, and you will need to find, modify and inject the specific file which determines your keycode mappings.

Thanks to the following resources which helped me put this together:
* http://gustavepate.github.io/blog/20130714/android-keyboard-layout-logitech-tablet-keyboard/
* https://developer.android.com/reference/android/view/KeyEvent
* https://source.android.com/devices/input/key-character-map-files
* https://forum.xda-developers.com/t/how-to-remap-mouse-buttons-and-is-possible-to-make-kl-and-kcm-files-for-it.3190940/
* https://topjohnwu.github.io/Magisk/guides.html
