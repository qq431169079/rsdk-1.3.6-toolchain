# rsdk-1.3.6-toolchain
The Realtek SDK (RSDK) v1.3.6 Lexra toolchain (RTL8xxx SoC, LX5280, LXxxxx) and a shell source file to set your environment

## What is this

This is a toolchain provided by Realtek that is compatible with the MIPS based Lexra CPU, which doesn't implement unaligned loads and stores for patent reasons. This chip can be found in older embedded devices. The activate script is for convenience and will set up your environment to use the toolchain after copying it where you want it on your local filesystem

## Using

Using this to build something is pretty straightforward using the activate script in the root of the repository. Just place the activate script into the rsdk-1.3.6/ directory and copy the rsdk-1.3.6 directory to where you would like it to reside, i.e. /toolchains. At that point, ```source /toolchains/rsdk-1.3.6/activate``` and you are all set. You can then build software using ```configure``` style build systems, or via plain old ```gcc```. You should make use of the ```cross_configure``` alias

## Examples

### Use gcc to compile something by hand

```
$ gcc bah.c -o bah 
```

### Use a ```configure``` based build system

```
$ cross_configure
...
$ make -j
```

