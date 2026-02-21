# Kai Simple + Ploopy Adept combo, and now implemented with Prospector dongle (Zephyr 4.1), new status screens, and backlight control and lightoff when idle for the dongle!

To control dongle's backlight  simply put keycodes like `&bl BL_TOG`, `&bl BL_INC`, `&bl BL_DEC` in the keymap.

Here I'm having Prospector ZMK dongle as central, connecting to 3 peripherals, left & right split and the trackball.

![PXL_20260116_062725646~2](https://github.com/user-attachments/assets/970c92bf-cc5c-47c5-ad9e-16b22f8368f0)

Also able to reach 118Hz on average with dongle. Used to be less stable just connecting trackball's Xiao board via BLE.
<img width="2004" height="958" alt="image" src="https://github.com/user-attachments/assets/dc33b9ec-f3da-49fc-91cc-1eaf15f41cff" />

I used to seperate them and connect them individually, why bundle them together after all this time?
- I want to use keyboard keys for mouse clicks and let my right hand, which is on the trackball, to fully focus on moving the cursor. IMO this is more ergonomic.

What's good about ZMK dongles?<br/>
- Almost immediate connection and wake-up from sleep mode.<br/>
- No more dependent from less stable Bluetooth connections.<br/>
- Extended battery life for both splits/peripherals.<br/>
- "Wireless" support for ZMK studio, able to change keymaps on the fly.<br/>

Surely there's something bad?<br/>
- Extra cost for a spare MCU, seeeduino nrf52840 sense in my case here.<br/>
- Takes up an extra USB slot on your device.

What I did in this branch:
- Follow new ZMK doc guide about LED backlight for Zephyr 4.1.
- Apply Xiao_ble_zmk pinouts.
- Add corresponding keycode to keymap.
- Add corresponding config to dongle.config.