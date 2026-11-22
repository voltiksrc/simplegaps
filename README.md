# simplegaps

A small patch for [dwl](https://codeberg.org/dwl/dwl) that adds configurable inner and outer gaps to the default tiling layout.

## Compatibility

Supports dwl v0.9 and the current development version (`main`). I haven't tested it on older versions.

## Installation

Clone dwl:

```sh
git clone https://codeberg.org/dwl/dwl.git
cd dwl
```

If you want to use dwl v0.9 instead of the development version, run:

```sh
git checkout v0.9
```

Download the appropriate `simplegaps.patch` for your version, place it in the dwl directory, and apply it:

```sh
git apply simplegaps.patch
```

If you don't already have a `config.h`, copy the default one:

```sh
cp config.def.h config.h
```

Then compile and install:

```sh
make
sudo make install
```

## Configuration

The default gap size is 12 pixels. You can change it in `config.h`:

```c
static const int gappx = 12;
```

Just change `12` to whatever you want and recompile.

## Limitations

Right now, gaps only work with the default `tile()` layout. Other layouts aren't supported yet.

It's a pretty simple patch, so there might still be some issues I haven't found.
