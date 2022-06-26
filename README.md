# Bare-Metal-Virtual-Emulator

## Description

The Bare Metal Virtual Emulator (BMVE) is a "virtual emulator" for bare metal
systems like the Raspberry Pi. Except that it's neither "virtual" nor an
"emulator" per se. That is, it neither virtualizes the instructions nor purely
emulates them.

Rather, it compiles the source code into x86, catches all memory accesses
dynamically, and emulates only those and the related devices.

This gives BMVE the advantage of being much faster than naive emulation.
However, it also therefore cannot emulate assembly at all without static
translation during compilation, or doing it dynamically (which would likely
be more of a hassle).

## Dependencies

1. [Intel XED](https://github.com/intelxed/xed)
   (included as a submodule and linked statically)

