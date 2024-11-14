# Atari 8-bit Git template repo

Use git straight from your Atari 8-bit computer. 

https://github.com/user-attachments/assets/e0558c34-0741-4e70-920e-98a72fade00e

The video shows [this commit](https://github.com/JSJvR/atari-8-bit-git-template/commit/14f69b4393901dea558b4a9ecce9b8b7189de932) being made from my Atari. Note that the [BASIC listing](https://github.com/JSJvR/atari-8-bit-git-template/blob/367d22375184d9a73c7c38c9ff049913a7ef558b/utf8/LOVE.LST) and the commit message both contain a "♥" which is `0x00` in ATASCII and therefore not valid in a standard text file. ATASCII characters  get translated automatically to their [closest Unicode equivalent](https://www.kreativekorp.com/charset/map/atascii/).

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

1. Create a git repo based on this template by whichever method you prefer, e.g. running `git init` locally, downloading the files from GitHub and copying them into your local repo. Since you're not going to push to this template repo, cloning it is probably not the way to go, unless you change your origin remote or if you don't plan to ever push.
1. Mount a disk image in the `atr` directory. Use the included `Example.atr` or replace it with your own.
1. From your PC, in base directory of your repo, run `a8utils atr2git`.
1. From your Atari or emulator, modify files on the mounted disk. 
1. When you're ready to commit, modify `COMMIT.MSG` with your commit message. 
1. Watch the magic happen. Two versions of each source file will be committed: the ATASCII original and a UTF-8 version that can easily be viewed on a modern computer. 


## Customize

Modify the `config` section of the `state.json` file. 

## Limitations

[Atari 8-bit Utils](https://github.com/JSJvR/atari-8-bit-utils) was a quick weekend project, so YMMV. 

Some of the limitations:
1. Only a single ATR image 
1. Only supports updating from the ATR image to files, not the other way around
1. Limted configurability, e.g. the directory structure is fixed

Depending on free time and motivation, I might change some of this in the future.

-----
This project is automatically managed using [Atari 8-bit Utils](https://github.com/JSJvR/atari-8-bit-utils)
