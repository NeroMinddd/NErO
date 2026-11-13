### Nikita (NErO)
`14 y.o.` | `Ring 0` | `Kernel Internals` | `Hardware Virtualization`

Low-level systems developer and reverse engineer. Focusing on OS kernel internals, hypervisor architecture, and bare-metal binary analysis.

Prefer reversing stripped binaries blindly—raw assembly, no PDB symbols, minimal external lookups.

---

### Current Focus
* **Type-2 Hypervisor (WIP):** Writing a lightweight Intel VT-x hypervisor from scratch (VMX initialization, VMCS state configuration, EPT paging, and shadow-page hooking).
* **Windows Memory Manager RE:** Blind disassembly and static analysis of `ntoskrnl.exe` routines (`IoAllocateMdl`, `MmProbeAndLockPages`) without symbols.
* **Kernel Exploitation & Mitigations:** Studying pool layouts, BYOVD vectors, DKOM, and hardware-enforced isolation (SMEP/SMAP, HVCI, VBS).

---

### Stack & Environment
* **Core:** Modern C++, x86-64 Assembly (Inline/Naked), Python (automation)
* **Hardware/Arch:** Intel VT-x/VMX, AMD-V, x86-64 Paging & Segmentation
* **RE & Debugging:** IDA Pro, Ghidra, WinDbg (KDNET), GDB, LLDB
* **OS Internals:** Windows Kernel (IRP, Pools, MDL, Drivers), Linux Kernel (Modules, SLUB, POSIX)

---

### Selected Work

**Intel HAXM Driver Audit & PoC (`IntelHaxm.sys`)**
* Reconstructed `DriverEntry` and IRP dispatch paths via raw offsets in `DRIVER_OBJECT` without PDBs.
* Identified out-of-bounds pointer arithmetic (`Base + Index * 0x18`) in unsigned `vcpuid` handling (**CVE-2022-21812**).
* Built a User-Mode C trigger targeting `METHOD_NEITHER` IOCTL gateways to interact with the kernel pool.

**x86-64 Assembly & ABI Research**
* Implementations of naked functions, custom shellcodes, and low-level context switching mechanics.
* Comparative analysis of Microsoft x64 vs. System V AMD64 calling conventions and Native API layouts.

**Async C++ Encrypted Messenger**
* Non-blocking event loop built on `Boost.Asio` with explicit lifetime management (`weak_ptr` / `enable_shared_from_this`), OpenSSL transport layer, and SQLite storage.

---

### Roadmap
1. Finish MVP of the custom Intel VT-x hypervisor and EPT hooking engine.
2. Build automated kernel-mode IOCTL fuzzers and continue blind audits of Windows Memory Manager components.
3. Develop a custom x86-64 OS kernel from scratch (bootloader, physical/virtual memory manager, lock-free scheduler).

##Connect

**Telegram:** [@NeroMind](https://t.me)
