# ZeroLag IPTV — Lightweight WPF IPTV Client

A fast, modern, and low-footprint IPTV desktop client built from scratch for Windows using **C# and WPF (.NET)**. Designed to handle large M3U/M3U8 playlists smoothly without UI freezes or excessive RAM consumption.

📥 **[Download Latest Release (Windows x64)](https://github.com/KosugeDev/zero-lag-iptv/releases/latest)**

---

### 🖼️ Screenshots


.
---

### ✨ Key Features

* **Fast M3U / M3U8 Parsing:** Asynchronous playlist loading and categorization (Live TV, Movies, Series).
* **Hardware-Accelerated Playback:** Smooth streaming with low latency and adaptive buffering.
* **Channel Search & Filtering:** Instant real-time filtering across thousands of channels.
* **Minimal Resource Footprint:** Optimized for low CPU and memory usage on Windows 10/11.

---

### 🏗️ Technical Architecture & Engineering Highlights

This repository serves as an architectural overview and binary distribution hub (closed-source freeware).

* **UI Framework & Pattern:** Built with **WPF** following clean separation of concerns (**MVVM**), utilizing data binding and asynchronous commands (`async/await`) to keep the UI thread completely responsive during network I/O.
* **UI Virtualization:** Implemented virtualized list containers (`VirtualizingStackPanel`) to render playlists containing 10,000+ channels with constant memory usage and zero scroll lag.
* **Stream & Parser Pipeline:** Custom asynchronous stream parser that processes M3U metadata tags (`tvg-logo`, `group-title`, `tvg-id`) using memory-efficient string handling rather than heavy DOM/object allocations.
* **Media Engine Integration:** WebView2 & LibVLCSharp for broad codec and HLS stream compatibility. The default media engine that primarily prevents latency is WebView2. However, if, in rare cases, some channels fail to open, LibVLCSharp can be assigned that specific channel. Additionally, LibVLCSharp can be optionally selected as the default media engine (not recommended for zero latency). This dual media player architecture ensures that every channel opens while leveraging the power of WebView2 to deliver zero latency and zero stuttering.
* **Packaging & Distribution:** Compiled as a self-contained single-file release with custom assembly metadata and SHA-256 integrity verification.

---

### 💻 System Requirements

* **OS:** Windows 10 / Windows 11 (64-bit)
* **Architecture:** x64

---

### 📄 License & Usage

* This software is distributed as **freeware** for personal use. Reverse engineering, decompilation, or commercial redistribution without permission is prohibited.
* Since this project has the potential to grow further and expand its services in the future, I am deliberately choosing not to share its source code and am keeping it closed-source.

### 📦 Release Notes
* Initial public release of **Zero Lag IPTV** for Windows (x64).
* Asynchronous M3U/M3U8 parsing and virtualized channel list rendering.
* Hardware-accelerated playback engine.

### 🔒 File Verification (SHA-256)
D8C9D9E3EC9D9FADD11D399C2BCC372E8260364F5D6BFD79FFDA9B8D337F3A4B

**Full Changelog**: https://github.com/KosugeDev/zero-lag-iptv/commits/v1.0.0

Disclaimer: Zero Lag IPTV is strictly a media player application. It does not provide, host, distribute, or include any playlists, channels, or media content. Users must supply their own legally obtained M3U/M3U8 streams.
