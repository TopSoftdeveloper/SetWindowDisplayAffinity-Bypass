
# SetWindowDisplayAffinity-Bypass : Bypassing Window Capture Protection on Windows (Educational)

## Overview

On Microsoft Windows, applications can restrict screen capturing by using the **`SetWindowDisplayAffinity`** API with the following flags:

* **`WDA_MONITOR`**
* **`WDA_EXCLUDEFROMCAPTURE`**

These flags are commonly used to prevent screenshots and screen recording by most capture tools (e.g. Print Screen, Snipping Tool, OBS, etc.).

This repository demonstrates a **non-invasive technique** to capture screenshots of such protected windows **without using DLL injection** or API hooking.

> ⚠️ **This project is strictly for educational and research purposes.**

---

## Background

Historically, developers attempting to bypass this protection have relied on:

* DLL injection into the target process
* Hooking `SetWindowDisplayAffinity` to modify or override its parameters

While effective, those approaches:

* Modify the target process
* Are intrusive and easier to detect
* Can introduce instability or security risks

This project explores an **alternative approach** that avoids injecting code into the protected application.

---

## Demonstration

The concept is inspired by and related to the following reference project:

🔗 **Reference:**
[https://github.com/wongfei/wda_monitor_trick](https://github.com/wongfei/wda_monitor_trick)

This repository builds upon the idea to show how screenshots can still be obtained under specific conditions, even when `WDA_MONITOR` or `WDA_EXCLUDEFROMCAPTURE` is enabled.

---

## Key Points

* ✅ No DLL injection
* ✅ No API hooking inside the target process
* ✅ Works on windows protected by `SetWindowDisplayAffinity`
* ❌ Not guaranteed to work on all Windows versions or GPU drivers
* ❌ Not intended for production or malicious usage

---

## Disclaimer

This project is provided **for educational and academic research only**.

You are responsible for:

* Complying with local laws and regulations
* Respecting software licenses and privacy policies
* Using this knowledge ethically

The author **does not condone** misuse of this technique for privacy invasion, DRM circumvention, or any illegal activity.

---

## Contact & Support

If you’d like to discuss the project or support future research:

* **Telegram**: [@somerwork](https://t.me/somerwork)
* **Donate (BTC)**:
  `bc1q43u0n865fuxc4j2vgm4wp98xuuaawgkgq8yrf4`
* **Donate(ETH,BEP)**:
  `0xE666B0517cb1Ae95982a1a80fAC0C65Df86B789a`
