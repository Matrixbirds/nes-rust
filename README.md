# nes-rust
learn rust and nest protocol

### NES Hardware Capabilities Spec
    * 8-bit 6502 CPU running at 1.79 MHZ.
        * 3 general purpose register A/X/Y
        * 3 special register P(status) / SP (stack pointer) / PC (program counter, or instruction pointer)

    * 16-bit addressable memory space
        * it can address 64k memory however it only has 2kb onboard RAM
        * rest is either not wired up (mirros of those 2kb), or mapped to special I/O registers, or catridge ROM/RAM space.

    * PPU (Picture Processing Uint)
        * supporting rendering 256x240 screen composed of 8x8 tiles for background.
        * up to 64 8x8 or 8x16 sprites for moving objects.
        * support pixel-level scrolling (which is big deal back in that day)

    * APU (Audio Processing Uint)
        * 2 pulse channel
        * 1 triangle channel
        * 1 noise channel
        * 1 DMC(delta modulation) channel.
        * One can still make good music with these - just not great sound effects.

    * Controllers
        * from classic NES controller or NES mouse.

    * Catridge (mappers)
        * its mean ROMsm (sometimes own battery-backed RAM, or own audio processing unit)
        * the dynamically maps ROM/RAM into CPU and PPU memory space, bypassing the limitation of 16-bit address space.
        * Some catridge come with more than 256kb of CHR ROM and swap/map portion of it on demand
