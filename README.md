
# SetWindowDisplayAffinity-Bypass : Bypassing Window Capture Protection on Windows (Final Version)

## Previous Research
* Driver solution is ready in https://github.com/TopSoftdeveloper/Bypass-SetWindowDisplayAffinity

## Overview

On Microsoft Windows, applications can restrict screen capturing by using the **`SetWindowDisplayAffinity`** API with the following flags:

* **`WDA_MONITOR`**
* **`WDA_EXCLUDEFROMCAPTURE`**

These flags are commonly used to prevent screenshots and screen recording by most capture tools (e.g. Print Screen, Snipping Tool, OBS, etc.).

This repository demonstrates a **non-invasive technique** to capture screenshots of such protected windows **without using DLL injection** or API hooking.

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
## Result

Check video.mp4 file to understand how it works.

## Contact & Support

If you’d like to discuss the project or support future research:

* **Telegram**: [@somerwork](https://t.me/somerwork)
* **Donate (BTC)**:
  `bc1q43u0n865fuxc4j2vgm4wp98xuuaawgkgq8yrf4`
* **Donate(ETH,BEP)**:
  `0xE666B0517cb1Ae95982a1a80fAC0C65Df86B789a`
