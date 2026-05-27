<div align="center">
  <img src="logo.png" width="180" alt="Magic Activator Pro Logo">
  <h1>Magic Activator Pro 🪄🔓</h1>
  <p><b>Freemium iCloud Activation Lock Bypass Tool for Windows and macOS.</b></p>

  <p>
    <img src="https://img.shields.io/badge/Version-1.2.2-blue.svg?style=for-the-badge" alt="Version">
    <img src="https://img.shields.io/badge/Model-Freemium-purple.svg?style=for-the-badge" alt="Freemium">
    <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-lightgrey.svg?style=for-the-badge" alt="Platform">
    <img src="https://img.shields.io/badge/Language-English%20%7C%20Spanish-green.svg?style=for-the-badge" alt="Language">
  </p>
</div>

---

### ✨ Overview

**Magic Activator Pro** is the professional evolution of iCloud bypassing and device activation recovery. Starting with **v1.2.2**, the project has transitioned from a strictly Premium model to a new **Freemium** model.

This new model allows users to test the service with limited free access while still keeping paid licenses available for full, permanent device registration.

Spiritual successor of the legendary redsn0w, currently supporting **iOS 17.0 – 18.7.2** and **iOS 26.0.1 through 26.1 and 26.2 Beta 1**! 🚀  
Support for Chinese devices (CH/A) is currently under evaluation and will be clarified in future updates.

> [!WARNING]
> **Use ONLY on devices you own or have permission to unlock.**  
> Bypassing iCloud violates Apple’s ToS – do it responsibly.

---

<div align="center">
  <h2>💎 Freemium Access & Registration</h2>
</div>

Magic Activator Pro is now **Freemium**.

The Freemium model allows users to register **one device once every 24 hours**. After the 24-hour freemium access window has been used, users must purchase a paid license to continue using registered workflows.

Your support through paid registration is vital; it directly funds server infrastructure, compatibility research, exploit development, and future support for currently unsupported versions like **iOS 18.7.3+** and **iOS 26.2 Beta 2+**.

| Access Type | Details |
| :--- | :--- |
| **Freemium Access** | 1 device registration allowed every 24 hours |
| **Cooldown** | Once used, free registration cannot be reused until the 24-hour window resets |
| **Paid License** | Required after the freemium window or for full/permanent registered access |
| **License Type** | Serial Number (SN) based registration |
| **Paid Cost** | $5.00 USD per device |
| **Paid Access** | Permanent registration for the processed SN with unlimited re-activations on the same device |
| **Registration Panel** | https://magicstore.pro/index.php |

> [!IMPORTANT]
> Freemium does **not** mean unlimited free usage.  
> Free access is limited to **one device registration every 24 hours**. After that, a paid license is required.

---

<div align="center">
  <h2>🆕 Changelog (v1.2.2) 🛠️</h2>
</div>

* **Premium → Freemium Transition:** Magic Activator Pro now supports a Freemium model with one free device registration every 24 hours.
* **Paid License System Preserved:** After the freemium registration window is used, users must purchase a paid license for continued registered access.
* **RAM-Only Registration Verification:** Replaced old log-based verification with secure `check_sn.php` validation directly in memory.
* **Origin-Isolated Registration:** Activator registration now uses `origin=activator` to separate it from other Magic software products.
* **Safe Action Log:** Serial numbers, UDID, ECID, IMEI, and sensitive URLs are now hidden from user-facing logs.
* **Registration Status Pill:** Added modern status indicators such as Verified, Pending, Not Registered, Server Unavailable, Invalid Response, and Checking.
* **Recheck Registration Button:** Added a small reload button beside the registration status for manual verification.
* **Liquid Glass V3 Interface:** Introduced a redesigned glass-style UI for a cleaner and more modern look.
* **iOS-Style Black Dark Mode:** Replaced the older blue/dark theme with a true black graphite-style interface.
* **Adaptive Device Image Card:** Device image preview now resizes intelligently based on window size and available space.
* **Safe Device Image Shadow:** Added a smoother shadow behind the device image without using unstable rendering methods.
* **Performance Profiles:** Added visual quality modes for smoother behavior on low-end hardware.
* **Crash Guard & Runtime Logs:** Added safer internal crash/runtime logging with sensitive-data masking.
* **macOS Alignment:** macOS edition now visually matches the Windows Liquid Glass V3 interface.
* **Improved Stability:** Better handling of stale registration responses, workflow locks, device refresh errors, and UI redraws.
* **OTA & Server Synergy:** Optimized OTA block operations and unified server-side support checks.

---

<div align="center">
  <h2>⚠️ IMPORTANT – Required Dependencies</h2>
</div>

> [!IMPORTANT]
> **Magic Activator Pro requires Python to work correctly.**

### Windows

1. **Download and install Python 3.11.9 (64-bit)**  
   → https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe

   ☑️ **IMPORTANT:** During installation, check:

   ```txt
   Add Python to PATH
   ```

2. **Install pymobiledevice3**  
   Open CMD as Administrator and run:

   ```bash
   pip install pymobiledevice3==6.1.5
   ```

### macOS

Magic Activator Pro for macOS requires a valid Python 3.11.9 installation.

The app rejects `/usr/bin/python3` because it is the macOS system Python and should not be used for this workflow.

Recommended Python path:

```txt
/Library/Frameworks/Python.framework/Versions/3.11/bin/python3.11
```

Install `pymobiledevice3`:

```bash
/Library/Frameworks/Python.framework/Versions/3.11/bin/python3.11 -m pip install pymobiledevice3==6.1.5
```

---

<div align="center">
  <h2>📱 Compatibility</h2>
</div>

| Category | Supported |
| :--- | :--- |
| **Supported Versions** | iOS 17.0 → iOS 18.7.2 / iOS 26.0.1, 26.1, and 26.2 Beta 1 ✅ |
| **NOT Supported Yet** | iOS 18.7.3+ and iOS 26.2 Beta 2+ (Researching exploits) ⚠️ |
| **Devices** | A12 → A19 (iPhone Xs → iPhone 17/Air series & compatible iPads) |
| **Best regions** | Global Support (LL/A, EU, ASIA) 🌎 |
| **Platform** | Windows 10/11 (64-bit) & macOS 🖥️🍎 |

> [!NOTE]
> Compatibility may vary depending on build, region, device state, support files, and server-side status.

---

<div align="center">
  <h2>🛠️ How It Works (Technical Deep Dive)</h2>
</div>

1. Connect device via USB in normal mode 🔌
2. Tool reads ECID, model, region, serial number, and iOS build 🔍
3. The app verifies registration status using RAM-only SN validation through `check_sn.php` 🔐
4. If available, Freemium access allows **one registration every 24 hours** ⏳
5. If the freemium window has already been used, a paid license is required 💳
6. Provide exact **MobileGestalt + supporting files** when requested 📁
7. Magic server generates the required activation data 🎟️
8. Record gets injected → device activated successfully 🎉
9. OTA updates can be blocked after completion 🛡️

> [!TIP]
> **Success time:** 3–7 minutes ⏱️  
> **>10 min = abort & retry after cooldown**

---

<div align="center">
  <h2>🔥 Features</h2>
</div>

- **Freemium Access:** One free device registration every 24 hours. ⏳
- **Paid License Support:** Permanent registration available for full access. 💳
- **RAM-Only Registration Check:** Safer SN verification without downloading registration logs. 🧠
- **Privacy-Safe Logs:** Sensitive identifiers are hidden from the user-facing Action Log. 🧼
- **Liquid Glass V3 Interface:** Modern glass-style UI with improved cards, buttons, and shadows. 🎨
- **iOS-Style Dark Mode:** True black/graphite dark mode. 🌑
- **Adaptive Device Preview:** Device image resizes intelligently with the app window. 📱
- **Integrated Extractor:** Native data gathering for smoother processing.
- **No jailbreak required** 🚫
- **Real-time detailed logs** 📜
- **OTA block** 🛑
- **tvOS profile sideloading** 📺
- **Support file checker** 📁
- **Hidden Dev Mode tools** 🧰
- **Crash/runtime protection** 🛡️
- **Performance profiles for low-end hardware** ⚡
- **Weekly updates during beta season** ⚡

---

<div align="center">
  <h2>🚀 Installation & Usage</h2>
</div>

1. Download latest build (**v1.2.2**)
2. Install required dependencies if prompted.
3. Run as Administrator on Windows / open normally on macOS and allow required permissions 👑
4. Connect your device via USB in normal mode.
5. Wait for device detection.
6. Check the registration status pill.
7. Use Freemium registration if available.
8. If the 24-hour free registration has already been used, register a paid license → https://magicstore.pro/index.php
9. Use Wi-Fi, select the correct workflow, and wait for the magic 🎇

---

<div align="center">
  <h2>⚠️ Current Limitations</h2>
</div>

- Freemium access is limited to **one device registration every 24 hours**.
- After the free registration window is used, a paid license is required.
- No full iCloud services (Drive, Find My, etc.)
- No push notifications on some builds.
- Calls/SMS may be broken on GSM devices.
- iOS 18.7.3+ / iOS 26.2 Beta 2+ → currently **NOT supported** (Research in progress).
- Compatibility depends on available support files and server-side status.

---

<div align="center">
  <h2>❓ Issues</h2>
</div>

**idk, u tell me!**  
Found a bug? Missing your region/build? Want a new feature?  
→ Open an **Issue** here on GitHub and I’ll check it as soon as possible! 🛠️

When reporting issues, include:

- Device model
- iOS version
- Build number
- Platform used
- Screenshot if possible
- Sanitized log if available

> [!CAUTION]
> Do not post full serial numbers, UDIDs, IMEIs, ECIDs, or private device data.

---

<div align="center">
  <h2>❤️ Support & Future Development</h2>
</div>

Freemium access and paid registrations directly support the research and development of the next big features:

- Research and integration of the latest exploits for **iOS 18.7.3+** and **iOS 26.2+**.
- Push notifications fix 📲
- Partial iServices restoration experiments
- macOS and Windows build improvements
- Server infrastructure and support-file hosting
- Stabilization for rare regions 🌍
- Better low-end hardware performance ⚡

All future builds & changelogs will be published right here on GitHub.

**Contact & Support:**

* 🌐 **Web:** [https://magicstore.pro/](https://magicstore.pro/)
* 𝕏 **X (Twitter):** [x.com/magicactivator](https://x.com/magicactivator)
* 💬 **WhatsApp Support:** [+504 9291-2204](https://wa.me/50492912204)

---

<div align="center">
  <h2>🗺️ Roadmap (Actively in Development)</h2>
</div>

- Ongoing research for iOS 18.7.3+ and iOS 26.2+ (Beta 2+) exploits.
- Improved Freemium registration flow.
- Better low-end hardware performance.
- More stable macOS builds 🍎
- More unified Magic software suite design.
- ~~Native macOS version 🍎~~
- ~~Built-in MobileGestalt extractor~~
- Misaka26/TrollStore integration research.

---

<div align="center">
  <h2>🖼️ Screenshots</h2>

  <h3>Windows Port</h3>
  <img src="Screenshot.png" width="600">
  
  <br><br>

  <h3>macOS Port</h3>
  <img src="Screenshot-2.png" width="600">
</div>

---

<div align="center">
  <h2>❤️ Credits & Love</h2>
</div>

- Lead developer: @DarkboyBeyond (Honduras 🇭🇳)
- Inspired by redsn0w, checkra1n & the old jailbreak legends
- Huge thanks to every file contributor and tester!

### License

Proprietary binaries.  
Changelogs, docs & community files: MIT.

**Magic Activator Pro – Freemium, safer, cleaner, and redesigned for v1.2.2.**  
**One free registration every 24 hours. Paid license required after the freemium window.**  
Follow @DarkboyBeyond_ on X for instant updates! 🪄✨

*Last updated: March 15, 2026*
