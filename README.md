# SDKernelFuzzing
Kernel Fuzzing driven by System call(Syscall) Dependency graph

## Introduction
Kernel Fuzzing driven by System call Dependency graph contain 2 submodule:
1. (LKSAST)static analysis to construct the System call Dependency graph
2. (sysdepller)kernel fuzzing driven by System call Dependency graph

## How to build and build
```shell
git submodule init
git submodule update
```
It will clone 2 git repo into workspace
1. https://github.com/LittleSec/LKSAST in workspace
2. https://github.com/LittleSec/sysdepller in src/github.com/google

By the way, sysdepller is fork from google/syzkaller and it has a huge size and network always slow(with git submodule which do not support clone which `--depth` option), so I ***recommand*** clone/download each repo with option `--depth 1`

```shell
git clone https://github.com/LittleSec/LKSAST
git clone --depth 1 https://github.com/LittleSec/sysdepller src/github.com/google/sysdepller
```

And then see their README.md to build and run.

These tools run ***independently***, running LKSAST first and then sysdepller

## TODO

add more detail