<div align="center">

# ⚡ ZeroLag IPTV

**A high-speed, dual-engine Windows IPTV player built for instant channel zapping, universal aspect-ratio fitting, and seamless remote control navigation.**

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011%20(x64)-0078D6?style=flat-square&logo=windows)](https://github.com/KosugeDev/zero-lag-iptv/releases/latest)
[![Framework](https://img.shields.io/badge/Built%20With-C%23%20%7C%20WPF%20(.NET)-512BD4?style=flat-square&logo=dotnet)](https://github.com/KosugeDev/zero-lag-iptv)
[![License](https://img.shields.io/badge/License-Freeware%20(Closed--Source)-lightgrey?style=flat-square)](#-license--legal-disclaimer)
[![Release](https://img.shields.io/github/v/release/KosugeDev/zero-lag-iptv?style=flat-square&color=success)](https://github.com/KosugeDev/zero-lag-iptv/releases/latest)

<br>

📥 **[Download Latest Release (Windows x64)](https://github.com/KosugeDev/zero-lag-iptv/releases/latest)**

</div>

---

## 📖 Overview

**ZeroLag IPTV** is a lightweight, performance-engineered desktop IPTV client developed from scratch in **C# and WPF (.NET)**. Unlike conventional players that suffer from sluggish channel switching, buffering delays, codec failures, or rigid aspect ratios, ZeroLag combines a hybrid playback pipeline with smart local caching to deliver near-instant channel zapping and smooth, stutter-free playback even on massive playlists.

---

## 🖼️ Screenshots

| Modern Player & Channel List | Themes & Customization |
| :---: | :---: |
| ![Main Interface](https://via.placeholder.com/600x340/0f172a/38bdf8?text=Main+Player+Screenshot) | ![Theme Menu](https://via.placeholder.com/600x340/0f172a/38bdf8?text=Themes+%26+Settings+Screenshot) |

---

## ✨ Key Features

* **⚡ Sub-Second Startup (`<1s`):** Smart local caching (`%LocalAppData%\ZeroLag IPTV\v2.0`) eliminates cold-start bottlenecks, launching **8x faster** (under 1 second after initial run).
* **🔄 Dual-Engine Playback (WebView2 + LibVLC):** Uses **Microsoft Edge WebView2** by default for ultra-low latency and instant channel zapping, while automatically falling back to **LibVLCSharp** whenever an unsupported stream or codec is encountered—ensuring channels always play. *(Default engine can also be switched manually in Settings).*
* **🖥️ Universal Fullscreen & Aspect-Ratio Stretching:** Eliminates black bars on any screen geometry. Dynamically stretches and fits streams seamlessly across **16:9** monitors, **21:9** ultrawide displays, and legacy **4:3 CRT** screens.
* **📡 Xtream Codes & URL & M3U/M3U8 Support:** Load your playlists effortlessly via **Xtream Codes API**, direct stream URLs, or local `.m3u` / `.m3u8` files with automatic categorization (Live TV, Movies, Series).
* **🎮 Universal Remote Control Support:** Native media-key and universal remote integration lets you change channels and control playback from your smartphone or external remote apps—no keyboard required.
* **🎨 Modern UI & Custom Themes:** Sleek, distraction-free interface featuring switchable themes: **Blue** *(Default)*, **Dark**, and **Classic Purple**.
* **🌍 Multi-Language Support (EN / TR):** Automatically detects your Windows OS language on first launch (defaults to English if non-Turkish) and can be switched anytime via `Settings > Language`.
* **👋 Quick First-Time Onboarding:** Automatically prompts the **Add Channel Source** menu on fresh installations with zero channels configured, getting you watching immediately.

---

## 🏗️ Technical Architecture & Engineering Highlights

This repository serves as the official documentation and binary distribution hub for **ZeroLag IPTV** (distributed as closed-source freeware).

* **Clean MVVM & Async Pipeline:** Built on WPF following strict **MVVM** separation of concerns. All network I/O, playlist parsing, and stream handoffs execute asynchronously (`async/await`) to keep the UI thread 100% responsive.
* **UI Virtualization at Scale:** Utilizes virtualized list containers (`VirtualizingStackPanel`) to render playlists exceeding **10,000+ channels** with constant memory overhead and zero scroll lag.
* **Hybrid Media Engine Orchestration:** Combines hardware-accelerated **WebView2** rendering for low-latency HLS/web streams with **LibVLCSharp** native decoding fallback, balancing zapping speed with universal codec compatibility.
* **Memory-Efficient M3U Parser:** Custom asynchronous stream parser that extracts metadata tags (`tvg-logo`, `group-title`, `tvg-id`) using low-allocation string processing rather than heavy DOM/object trees.
* **Persistent Local Caching:** Caches runtime assemblies and parsed workspace state in `%LocalAppData%\ZeroLag IPTV\v2.0`, cutting subsequent initialization times from ~8 seconds down to under 1 second.

---

## 🚀 Getting Started

1. Go to the **[Latest Release](https://github.com/KosugeDev/zero-lag-iptv/releases/latest)** page and download the `.exe` binary.
2. Run `ZeroLagIPTV.exe` *(No complex installer required)*.
   * *Note: Because the binary is independently published without a commercial EV certificate, Windows SmartScreen may display a prompt on first launch. Click **More info → Run anyway** to proceed.*
3. On first launch, enter your **Xtream Codes** credentials, **M3U URL**, or select a local `.m3u/.m3u8` file to start watching.

---

## 💻 System Requirements

* **Operating System:** Windows 10 (version 1809 or later) / Windows 11
* **Architecture:** 64-bit (`x64`)
* **Runtime:** Microsoft Edge WebView2 Runtime *(Pre-installed on Windows 11 and modern Windows 10 builds)*

---

## 📄 License & Legal Disclaimer

* **License:** Distributed as **freeware** for personal, non-commercial use. Reverse engineering, decompilation, modification, or commercial redistribution without explicit permission from the author is strictly prohibited. Source code is kept closed-source.
* **Disclaimer:** **ZeroLag IPTV is strictly a media player application.** It does not provide, host, distribute, or include any playlists, TV channels, or copyrighted media content. Users are solely responsible for supplying their own legally obtained streams or playlist sources.
