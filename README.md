# 🎨 Visual Studio light theme for IDA Pro
The modern light theme inspired by the Visual Studio. This is entirely based on an awesome [dp701](https://github.com/pr701/dp701/tree/main) theme by [pr701](https://github.com/pr701)

# 📝 Features

- Multiple sizes for different DPI
- Attention to detail

# 👁️‍🗨️ Preview

![](https://github.com/user-attachments/assets/73c7f150-34b6-4472-8925-ea93a33409f3)

# 📃 Requirements

- IDA version **7.3** or newer
- Installed **Segoe UI** and **Consolas** fonts

# 🛠️ Installation

## Installing the theme

- Copy the contents of `theme/*` into the IDA directory `themes/*`
- Start IDA and select the theme by to the screen resolution in `Options > Colors...`

## Change the font

The font has already been set in the theme file, but you can also manually edit it by opening `theme.css` and navigating to the block `Block for personalization` at the end of the file.

### A known issue

There is a bug in the IDA that resets the parameters from the `CSS` for fonts.

The current solution is setting the font (**Consolas**) for the disassembler window in `Options > Font...`.  or just apply [reg](https://wiki.winehq.org/Regedit) file (for Windows):

```ini
Windows Registry Editor Version 5.00

; Delete IDA fonts configuration
[-HKEY_CURRENT_USER\SOFTWARE\Hex-Rays\IDA\Font]
```

## Color settings for other plugins

Pre-calculated color settings for plugins.

### deREferencing

For the [deREferencing](https://github.com/danigargu/deREferencing) plugin, change the specified settings in the file `deferencing/config.py`:

```python
highlight_changes = True
highlight_color   = 0xc08933
```

## Optional for Windows 10

**Windows 10** only.

### Change the color of active and inactive title bars

These options will change your desktop window settings.

- Apply the [reg](https://wiki.winehq.org/Regedit) file:

  ```ini
  Windows Registry Editor Version 5.00
  
  ; Automatically Pick a Color from your Background
  [HKEY_CURRENT_USER\Control Panel\Desktop]
  "AutoColorization"=dword:00000000
  ; Active/Inactive Window Title Bar
  [HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\DWM]
  "AccentColor"=dword:ff302d2d
  "AccentColorInactive"=dword:ff494949
  ; Show accent color on the following surfaces
  ; Start, taskbar, and action center
  [HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize]
  "ColorPrevalence"=dword:00000001
  ; Title bars
  [HKEY_CURRENT_USER\Software\Microsoft\Windows\DWM]
  "ColorPrevalence"=dword:00000001
  ```

# 🔎 Screenshots

Even more screenshots for your pleasure :3

## Colors

![](https://github.com/user-attachments/assets/97709902-e28d-486c-a857-a9c4eba8296b)

## Debug

![](https://github.com/user-attachments/assets/2a38899e-790e-43c8-8f2c-149e43f36807)

## Hex

![](https://github.com/user-attachments/assets/0e78d173-a394-4519-9edf-b8a6a0406b51)

## Options

![options](https://github.com/user-attachments/assets/2cd6079e-38d0-436b-9848-627393036a42)

# Credits
[pr701](https://github.com/pr701) - an original [dp701](https://github.com/pr701/dp701)'s creator.
