# RickRollOS
A small kernel written in rust, that rickrolls the user upon boot, ~~built~~ copy pasted from this tutorial: https://os.phil-opp.com/

To run it on linux with QEMU, or just a .bin file:
```
git clone https://github.com/alx365/RickRollOS/
cd RickRollOS
rustup target add thumbv7em-none-eabihf
rustup override add nightly.
cargo install cargo-xbuild
cargo install bootimage
rustup component add llvm-tools-preview
cargo bootimage
qemu-system-x86_64 -drive format=raw,file=target/x86_64-blog_os/debug/bootimage-os.bin
```
You probably want to adjust the delay in the for loop in vga_buffer.rs, to match your needs.

Screenshot:
https://i.imgur.com/nlEbZCq.png

https://i.imgur.com/ivyNuy7.png
