# Build Emacs on macOS

## preparation

```bash
brew install autoconf automake texinfo jansson mailutils libxml2
```

### libxml2 setting(newer macOS requires following settings)

```bash
export LDFLAG="-L/usr/local/opt/libxml2/lib"
export CPPFLAGS="-I/usr/local/opt/libxml2/include"
export PKG_CONFIG_PATH="/usr/local/opt/libxml2/lib/pkgconfig"
```

## How to configure and build

```bash
autogen.sh
./configure --without-x --with-ns
make
make install
```

And copy `Emacs.app` to target directory
