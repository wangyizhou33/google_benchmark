### Build instruction

```sh
    conan install . --output-folder=build --build=missing
    cd build
    cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
    cmake --build . --config Release
    ./my_executable
```

Expected output
```sh
    2023-12-11T09:59:58-08:00
    Running ./my_executable
    Run on (12 X 3600 MHz CPU s)
    CPU Caches:
    L1 Data 32 KiB (x6)
    L1 Instruction 32 KiB (x6)
    L2 Unified 512 KiB (x6)
    L3 Unified 16384 KiB (x2)
    Load Average: 0.39, 0.48, 0.43
    ***WARNING*** CPU scaling is enabled, the benchmark real time measurements may be noisy and will incur extra overhead.
    ------------------------------------------------------------
    Benchmark                  Time             CPU   Iterations
    ------------------------------------------------------------
    BM_StringCreation      0.000 ns        0.000 ns   1000000000
    BM_StringCopy           3.71 ns         3.71 ns    188857325
```