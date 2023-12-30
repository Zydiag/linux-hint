# Linux

## Changing Caps to escape

- Xorg.conf

  You can achieve this by editing the file `/etc/X11/xorg.conf.d/00-keyboard.conf.`

  Example file:

  ```Section "InputClass"
          Identifier      "system-keyboard"
          MatchIsKeyboard     "on"
          Option          "XkbLayout" "us"
          Option          "XkbModel"  "pc104"
          Option          "XkbOptions" "caps:swapescape"
  EndSection
  ```

  **don't forget to restart X**

- if you want temporary solution or you have xinit file use
  `setxkbmap -option caps:swapescape`

## Natural Scroll

- temporary of in init file
  xinput set-prop 14 318 1
- libinput.conf
  sudo nvim /usr/share/X11/xorg.conf.d/30-touchpad.conf
  ```
  Section "InputClass"
      Identifier "touchpad"
      MatchIsTouchpad "on"
      Option "NaturalScrolling" "true"
  EndSection
  ```
