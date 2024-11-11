# Atari 8-bit Git template repo

Use git straight from your Atari 8-bit computer. 

## Requirements

1. A modern computer running a Windows or UNIX based OS.
1. Python >= 3.8.
1. [Atari 8-bit Utils](https://github.com/JSJvR/atari-8-bit-utils) - install by running `pip install atari-8-bit-utils`.
1. A version of [`mkatr`](https://github.com/dmsc/mkatr) compiled for you platform. The `lsatr` command must be in your `PATH`. 
1. A way to use an [ATR](http://fileformats.archiveteam.org/wiki/ATR) disk image on your computer, e.g. one of the following: 
   1. Mounting from your Atari using a [FujiNet](https://fujinet.online/) and a [TNFS server](https://github.com/FujiNetWIFI/tnfsd/releases) running on your PC.
   1. A [SIO2PC](https://www.atarimax.com/sio2pc/documentation/index.html) device connected to your PC. 
   1. An Atari emulator, e.g. [Altirra](https://www.virtualdub.org/altirra.html)
## Getting started

1. Create a git repo based on this template by whichever method you prefer, e.g. forking the project or running `git init` and downloading the files from GitHub.
1. Mount a disk image in the `atr` directory. Use the included `Example.atr` or replace it with your own.
1. From your PC, in base directory of your repo, run `a8utils atr2git`.
1. From your Atari, modify files on the mounted disk, and when you're ready to commit, modify `COMMIT.MSG` with your commit message. 
1. Watch the magic happen. Two versions of each source file will be committed, the ATASCII original and a UTF-8 version that can easily be viewed on a modern computer. 


## Customize

Modify the `config` section of the `state.json` file. 

## Limitations

[Atari 8-bit Utils](https://github.com/JSJvR/atari-8-bit-utils) was a quick weekend project, so YMMV. The biggest current limitation id that directories aren't supported. Only files in the root folder will be converted to UTF-8 andf committed. 


**Please retain everything below the line when copyping or forking this repo**

-----
This project is automatically managed using [Atari 8-bit Utils](https://github.com/JSJvR/atari-8-bit-utils)