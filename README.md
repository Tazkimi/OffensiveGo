# OffensiveGo - Golang Weaponization for red teamers.

![image](https://user-images.githubusercontent.com/75935486/220217814-242de1ba-1f62-4b0b-a1be-6cf8b82ab0da.png)


**This repo contains some examples of offensives tools & utilities rewrote in Golang that can be used in a red team engagement.**

## Table of Content

- [Previous work](#previous-work)
- [About Golang](#about-golang)  
  - [Installation](#installation)
  - [Compilation](#compilation)
- [Examples](#examples)
- [Interesting Tools in Golang](#interesting-tools-in-golang)
- [Credits](#credits)

## Previous work

These repo inspires me to make [OffensiveGo](https://github.com/RistBS/OffensiveGo)

- [OffensiveRust](https://github.com/trickster0/OffensiveRust) : Made by [trickster012](https://twitter.com/trickster012), this project contains a bunch of examples made in [Rust](https://www.rust-lang.org/).
- [OffensiveNim](https://github.com/byt3bl33d3r/OffensiveNim) : Made by [byt3bl33d3r](https://twitter.com/byt3bl33d3r), this one contains examples written in [Nim](https://nim-lang.org/).


## About Golang

- **Simpler syntax**: Go's syntax is simpler and easier to learn compared to Rust, which has a steeper learning curve.
- **Garbage collection**: Go uses garbage collection, which makes memory management easier for developers. Rust, on the other hand, uses a borrow checker to enforce memory safety, which can be more difficult to work with.
- **Cross-platform support**: Go has excellent cross-platform support and can be compiled to run on a wide range of platforms, including Windows, Linux, and macOS. Rust also has good cross-platform support, but its compilation process can be more complex.

**OPSEC Consideration & Caveats of Golang**


### Installation


### Compilation

`go build` for compilation 

Go binaries generally have no installation dependencies, compiler statically links Go runtime and needed packages. Static linking results in larger binaries


## Examples 

TODO : credits

| File                                                                                                   | Description                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Process Injection Native - APC](../main/injection_native_apc/main.go)        | Execute a shellcode with NtQueueUserApcThread  |
| [Process Injection Native - NtCreateThreadEx](../main/injection_native_thread/main.go)                         | Execute a shellcode with NtCreateThreadEx  |
| [API hashing](../main/api_hashing/main.go)                                                  | resolve APIs from EAT using DJB2 hashing algorithm (you can bring your own algorithm)  |
| [Whoami](../main/whoami/main.go)                                                  | rebuilt whoami process to show current user, groups & privileges   |
| [EnableDebugPrivileges](../main/enable_debug_priv/main.go)                                   | Enable SeDebugPrivilege in the current process    |
| [execute-assembly](../main/detect_hooks/main.go)                                                  | Loads CLR and execute .NET assemblies in memory  |
| [COFF loader](../main/coff_loader/main.go)                                                  | COFF loader to load PE files in memory   |
| [ACG + BlockDll](../main/acg_blockdll_process/main.go)                                                  | Apply Arbitrary Code Guard (ACG) & BlockDll policy on your process |
| [Process Argument Stomping](../main/process_arg_stomping/main.go)                                                  | Erase Process argument by parsing RtlUserProcessParameters  |
| [DNS over HTTP (DoH)](../main/dns_over_http/main.go)                                                  | A support of DNS over HTTP (DoH) for C2 communication  |
| [Detect Hooks](../main/detect_hooks/main.go)                                                 | Detect Hooks set by AV/EDR on NTDLL               |
| [Sleep Obfuscation](../main/sleep_obfuscation/main.go)                                                 | Perform Sleep Obfuscation with Queue Timers       |
| [AMSI Patching & Patchless](../main/amsi_bypasses/) | 2 Methods to bypass AMSI, first is to patch in memory with invalid value on AmsiScanBuffer, second is to use HWBP
| [ETW Patching & Patchless](../main/etw_bypasses/) | 2 Methods to bypass ETW, first is to patch in memory with ret on NtTraceControl, second is to use HWBP

## Interesting Tools in Golang

- [BananaPhone](https://github.com/C-Sto/BananaPhone) : An easy to use GO variant of [Hells gate](https://github.com/am0nsec/HellsGate) with automatic SSN parsing.
- [SourcePoint](https://github.com/Tylous/SourcePoint) : C2 profile generator for Cobalt Strike command and control servers designed to ensure evasion by reducing the Indicators of Compromise IoCs.
- [ScareCrow](https://github.com/optiv/ScareCrow) : Payload creation framework designed around EDR bypass such as AMSI & ETW Bypass, Encryption, Stealth Process Injections ect...
- [Freeze](https://github.com/optiv/Freeze) : Payload toolkit for bypassing EDRs using suspended processes, direct syscalls, and alternative execution methods.
- [Mangle](https://github.com/optiv/Mangle) : A tool that manipulates aspects of compiled executables (.exe or DLL) to avoid detection from EDRs.
- [Dent](https://github.com/optiv/Dent) : A framework for creating COM-based bypasses utilizing vulnerabilities in Microsoft's WDAPT sensors.
- [Ivy](https://github.com/optiv/Ivy) : Payload creation framework for the execution of arbitrary VBA (macro) source code directly in memory. Ivy’s loader does this by utilizing programmatical access in the VBA object environment to load, decrypt and execute shellcode.




## Credits

- [@BlueSentinelSec](https://twitter.com/BlueSentinelSec) - https://github.com/bluesentinelsec/OffensiveGoLang/blob/master/Offensive%20GoLang%202.0%20-%20SANS%20Pen%20Test%20HackFest%202021.pdf
