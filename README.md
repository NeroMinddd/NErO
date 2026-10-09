# NErO

# 👋 Hi, I'm Nikita (aka NErO)

### Low-Level Systems Developer • Reverse Engineering & Kernel Security Research (Ring 0)

I am a systems programmer focused on OS internals, binary analysis, and low-level software engineering. I specialize in understanding software-to-hardware interaction, working with CPU instructions, system calling conventions, and machine-level memory layouts.

---

## 🚀 Synopsis

- 💻 Programming since the age of **9**.
- ⚙️ Core Stack: **Modern C++ & x86-64 Assembly (Proficient)**.
- 🧩 Focus: **Systems Programming, Semantic Reverse Engineering, Kernel Architecture**.
- 🖥️ Platforms: In-depth study of Windows Internals & Linux Kernel structures.
- 🇬🇧 English: **B1 / Professional Working Proficiency (approaching B2)**.

---

## 🛠️ Tech Stack

- **Languages & Architectures:** Modern C++ (STL, Concurrency), x86-64 Assembly (Proficient — Inline Asm, Naked functions), Python (Automation & Scripting).
- **Architectures:** Intel VT-x/VMX, AMD-V, x86-64 Segmentation and Paging.
- **Reverse Engineering & Debugging:** IDA Pro, Ghidra, WinDbg (Kernel Debugging / KDNET), GDB, LLDB.
- **Systems & Technologies:** Windows Internals (IRP, Windows Kernel Pools, Driver Object Structures), Linux Kernel Architecture (POSIX, Modules, SLUB allocator), Boost.Asio (Asynchronous networking), OpenSSL, CMake, Ninja.

---

# 📂 Featured Systems Projects

## 🔬 Intel HAXM Kernel Driver Research & PoC
A deep static reverse engineering audit of the `IntelHaxm.sys` kernel-mode driver, focusing on undocumented internal mechanics and vulnerability analysis.
- **Reverse Engineering:** Reconstructed `DriverEntry` execution flow and tracked IRP routing mechanics via absolute pointer offsets inside the `DRIVER_OBJECT` table without PDB symbols.
- **Root Cause Analysis:** Audited host multiprocessor initialization sequences and mapped out-of-bounds pointer arithmetic (`Base + Index * 0x18`) affecting the unsigned `vcpuid` handling logic (CVE-2022-21812).
- **Exploitation:** Designed a robust User-Mode C software trigger (PoC) leveraging vulnerable IOCTL gateways (`METHOD_NEITHER`) to interact directly with the kernel pool.

## 💬 Asynchronous C++ Encrypted Messenger
A high-performance, asynchronous terminal-based communication engine built on modern C++ primitives.
- **Architecture:** Driven by a non-blocking event loop using **Boost.Asio**.
- **Memory Management:** Implements asynchronous execution pipelines with explicit object lifetime controls (`std::enable_shared_from_this`, `std::weak_ptr`) to ensure safety in concurrent state machines.
- **Crypto & Storage:** Network layer encryption via **OpenSSL**, standalone chat history storage with an optimized **SQLite** engine.

## 📦 Low-Level Assembly & Architecture Research
A collection of bare-metal and system-level code components written in pure **x86-64 Assembly**.
- Research on Calling Conventions (Microsoft x64 ABI vs System V AMD64 ABI), context switching logic, and software-to-hardware transition states.
- Implementation of Naked functions, custom shellcodes, and optimized cryptographic/string algorithms.
- Code analysis laboratories focused on parsing Native API structures and semantic binary audit.

## 🖥️ Linux Remote Administration Utility
A low-level C++ systems utility designed for secure remote server orchestration via POSIX APIs.

---

## 📚 Currently Researching (Current Focus)

- **Automated Vulnerability Discovery:** Designing architecture for custom kernel-mode IOCTL fuzzers on Windows.
- **Kernel Pool Exploitation:** Studying advanced pool layouts, exploitation primitives, and mitigation bypass techniques (BYOVD vectors, DKOM, Data-Only attacks).
- **OS Security Controls:** Deep dive into hardware-enforced isolation models (SMEP/SMAP, Hypervisor-Protected Code Integrity / HVCI, VBS).
- **Hardware Virtualization:** Low-level mechanics of Intel VMX (Root/Non-Root, VMCS configurations, EPT structures) in preparation for custom virtualization development.

## 🎯 Architectural Goals & Roadmap

1. **Phase 1 (Kernel & Automation):** Build reliable system-level automation testing tools (IOCTL fuzzers) and execute deep manual audits of modern peripheral drivers.
2. **Phase 2 (Virtualization):** Design and implement a **custom, lightweight Type-2 Hypervisor** from scratch, directly configuring VMX states, VMCS layouts, and EPT paging structures.
3. **Phase 3 (Operating System):** Build a **custom, security-hardened x86-64 Operating System** from the ground up (custom bootloader, physical/virtual memory management subsystem, and a race-condition-free task scheduler).

---

## 🤝 Connect

Interested in hardware architecture, systems software engineering, kernel research, or low-level binary analysis? Let's talk code.

**Telegram:** [@NeroMind](https://t.me)
