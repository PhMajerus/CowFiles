# Philippe Majerus's cowsay files collection


## Introduction

This repository contains the characters files ("cows") I created for the [cowsay/cowthink utility](https://en.wikipedia.org/wiki/Cowsay).
While original cowsay files are ASCII-art, I decided to experiment with ANSI/VT coloring, extended Unicode characters, pseudo-pixels (such as Unicode 13.0 sextants and Unicode 16.0 octants), and [Sixels](https://en.wikipedia.org/wiki/Sixel).


## Characters in this repository

### hellokitty
![hellokitty](images/hellokitty.png)

This uses extended Unicode characters and ANSI/VT colors (16 colors) and attributes (strikethrough, underline).
It is based on the Hello Kitty character by Yuko Shimizu / Sanrio.

### link
![link](images/link.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is inspired by the Famicom/NES game The legend of Zelda.

### sxl-cow
![sxl-cow](images/sxl-cow.png)

This uses a sixel image.
It is based on the cow sprite from the Super Famicom/SNES game Earthworm Jim.

The idea of this character is to provide a "HD remaster" of the original cow.
It can be used as a replacement for the ANSI-art cow used when `cowsay` is called without a `-f` option. To achieve this, rename the `default.cow` that ships with cowsay to `legacy-cow.cow`, and create a symbolic link `default.cow` pointing to `sxl-cow.cow` as follows:
```bash
cd /usr/share/cowsay/cows
sudo mv default.cow legacy-cow.cow
sudo ln -s sxl-cow.cow default.cow
```


## Installing & using cow files
You'll need the cowsay utility, so start with `sudo apt install cowsay` or equivalent for your distro.

Copy the files from this repo's `cows` folder to  `/usr/share/cowsay/cows`.

Then simply use the `cowsay -f [cow name] [message]` command.

---

-- Philippe Majerus, September 2024
