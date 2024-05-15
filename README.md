# Meson Bug Report (2024-05)

This is a toy example for a bug report for Meson (>=1.3.0rc1, <1.4.0).

```sh
$ meson setup build
$ meson compile -C build

INFO: autodetecting backend as ninja
INFO: calculating backend command to run: C:\msys64\ucrt64\bin\ninja.EXE -C D:/Code/Temp/demo0515/build
ninja: Entering directory `D:/Code/Temp/demo0515/build'
[3/6] Compiling Fortran object libtest1.a.p/src_kinds.F90.obj
FAILED: libtest1.a.p/src_kinds.F90.obj libtest1.a.p/kinds.mod
"gfortran" "-Ilibtest1.a.p" "-I." "-I.." "-fdiagnostics-color=always" "-D_FILE_OFFSET_BITS=64" "-Wall" "-O0" "-g" "" "-Jlibtest1.a.p" -o libtest1.a.p/src_kinds.F90.obj "-c" ../src/kinds.F90
gfortran: warning: : linker input file unused because linking not done
gfortran: error: : linker input file not found: No such file or directory
ninja: build stopped: subcommand failed.
```
