# MemoryModulePP

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

MemoryModulePP, used to load a DLL from memory. MemoryModulePP is compatible with Win32 API and supports exception handling.

**MemoryModulePP is developed based on [MemoryModule].**

**This repository is under development.**

# Features
  - Compatible with Win32 API (GetModuleHandleA/W/Ex GetModuleFileNameA/W/Ex GetProcAddress)
  - Support for C ++ exceptions and SEH
  - Compatible with Win7(x64) and Win10(x64)
  - Optimized MEMORYMODULE structure
  - Use reference counting, repeated loading of the same module will update the reference counting, please refer to NtLoadDllMemoryExW
  - The above features can be turned off through the dwFlags parameter of NtLoadDllMemoryExW

### Tech

MemoryModulePP uses many open source projects and references to work properly:

* [Vergilius Project][ref1] - Some windows kernel structure reference.
* [MemoryModule] - Load dll from memory, reference and improve part of this repository's code.
* [Blackbone][ref2] - Windows memory hacking library, Referenced the idea of exception handling.
* [Exceptions on Windows x64][ref3] - How Windows x64 Exception Handling Works. (Russian)

### Todos

 - Compatible with Win8 and x86 architecture
 - Improve MEMORYPODULE structure


   [MemoryModule]: <https://github.com/fancycode/MemoryModule.git>
   [ref1]: <https://www.vergiliusproject.com>
   [ref2]: <https://github.com/DarthTon/Blackbone.git>
   [ref3]: <https://habr.com/en/company/aladdinrd/blog/321868/>
   
