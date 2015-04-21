# arm-playground
## Install dependencies

```
brew install mpfr gmp libmpc libelf texinfo
```

## Install toolchain

```
git clone https://github.com/jsnyder/arm-eabi-toolchain
cd arm-eabi-toolchain
make install-cross
```

Soon it will probably fail...

### Fix GMP on failure

Remove the __need_size_t define and undef in gmp-h.in. It'll import ptrdiff_t
too, rather than just size_t.

### Continue building

```
make install-cross
```

Follow the instruction and install the commands in your shell.
I.e.  ` echo 'export PATH=/Users/robin/arm-cs-tools/bin:$PATH' >> ~/.zshrc`
