# Kai Simple + Ploopy Adept + Prospector combo!
Also with auto sleep and backlight control functions!</br>

<img src="https://github.com/user-attachments/assets/04c563fd-fb9f-43ab-af41-0a1877ead905" height=400></br>
<img src="https://github.com/user-attachments/assets/538fe97c-ebd7-4b54-905d-4e07acc5f020" height=400></br>

Features:</br>
✅ Prospector ST7789 dongle, with [4 screen options](https://github.com/carrefinho/prospector-zmk-module/tree/feat/new-status-screens)</br>
✅ ZMK Studio</br>
✅ Scroll with trackball</br>
✅ Up to 125Hz wireless transmission frequency (Bluetooth's highest limitation)</br>
✅ Cursor acceleration (faster you roll, faster you move)</br>

👉 [![Prospector Youtube demo](https://youtube.com/shorts/7Vw9d0dSeLg?feature=share/0.jpg)](https://youtube.com/shorts/7Vw9d0dSeLg?feature=share "Prospector Youtube demo") 🎞️</br>

To control dongle's backlight, simply put `&bl` keycodes in the keymap.</br>
[Here's the list for backlight action defines.](https://zmk.dev/docs/keymaps/behaviors/backlight#behavior-binding)</br>

What I did in this branch:</br>
- Follow [new ZMK doc guide about LED backlight for Zephyr 4.1.](https://zmk.dev/docs/development/hardware-integration/lighting/backlight)</br>
- Apply Xiao_ble_zmk pinouts.</br>
- Add corresponding keycode to keymap.</br>
- Add corresponding config to dongle.conf.</br>

Was able to reach 118Hz on average with dongle. Used to be less stable just connecting trackball's Xiao board via BLE.</br>
<img src="https://github.com/user-attachments/assets/dc33b9ec-f3da-49fc-91cc-1eaf15f41cff" height=300></br>

I used to seperate them and connect them individually, why bundle them together after all this time?</br>
- I want to use keyboard keys for mouse clicks and let my right hand, which is on the trackball, to fully focus on moving the cursor. IMO this is more ergonomic.</br>

What's good about ZMK dongles?<br/>
- Almost immediate connection and wake-up from sleep mode.<br/>
- No more dependent from less stable Bluetooth connections.<br/>
- Extended battery life for both splits/peripherals.<br/>
- "Wireless" support for ZMK studio, able to change keymaps on the fly.<br/>

Surely there's something bad?<br/>
- Extra cost for a spare MCU, seeeduino nrf52840 sense in my case here.<br/>
- Takes up an extra USB slot on your device.
