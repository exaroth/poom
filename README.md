<p align="center">
<img width="400" src="doom-builder.png"><br/><br/>
</p>

Doom builder is a simple tool for creating customized, self contained Doom executables running on [GZDoom](https://zdoom.org/index). You can run these as is or use them for testing custom community WADs.


## Installation

Download [doom-builder.zip](https://github.com/exaroth/doom-builder/releases/download/stable/doom-builder.zip) from [Releases](https://github.com/exaroth/doom-builder/releases/tag/stable) page and unzip.

## Usage

```
Usage: doom-builder <options>

Options:
  -f, --file          Path to pk3 or wad file to include.
  -w, --base-wad      Path to base wad/pk3 file.
  -h, --help          Print help.
```

To build custom Doom instance add list of WADs/pk3s you want to include via `-f` parameter as well as base Doom WAD (eg. the one included with Doom 1 or Doom 2 game). For example to build Doom executable running with Brutal Doom mod and custom OST run:

```
./doom-builder -f ./brutal_doom.pk3 -f /path/to/OST.WAD -w DOOM2.WAD
```

> [!IMPORTANT]
> :warning:   Doom builder will use shareware version of Doom by default if proper Doom 1/2 WAD is not provided via `--base-wad` parameter. Shareware version does not allow for using custom WAD files.

Doom Builder will create `doom` instance which, if executed without any parameters, will run Doom with provided custom wad files, additionally you can pass list of additional WADs as positional parameters, eg. using above example:

```
./doom ~/eviternity.wad
```

Will run Brutal Doom with custom OST and Eviternity mod.

## License

See `LICENSE` file for details
