# `mmap` vs. `read` in Rust, which is faster?

A small benchmark that reads files of various size from disk using either the `read` syscall (through `std::fs::read`), or by using `mmap` (using the `memmap2` crate). Also checks the effect that flushing the disk cache has on read performance (must be run as root). Runtimes are printed in milliseconds. 

Only works on Linux and MacOS.