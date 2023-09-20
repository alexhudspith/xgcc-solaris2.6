# xgcc-solaris2.6

A complete script to build a Sun Solaris 2.6 cross-compiler for 32-bit SPARC,
hosted on Linux x86-64.

The build produces GCC 4.3.6 which is the last version to support target
`sparc-sun-solaris2.6`.

## Building

1) Ensure you have satisfied the prerequisites below.
2) Execute `build` in the root directory.
3) The final executables can be found in `target/bin`.

## Prerequisites

1) A recent version of gcc running on Linux x86-64. The script was tested with
GCC 11.4.0.
2) A copy of the Sun Solaris 2.6 system headers and libraries. The script will
attempt to rsync these over ssh localhost:2222. This is suitable if you have set
up a QEMU system emulation using `qemu-system-sparc`, and you have forwarded host
port 2222 to the target ssh port 22. 
