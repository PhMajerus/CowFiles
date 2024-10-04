# Philippe Majerus's cowsay files collection


## Introduction

This repository contains the characters files ("cows") I created for the [cowsay/cowthink utility](https://en.wikipedia.org/wiki/Cowsay).
While original cowsay files are ASCII-art, I decided to experiment with ANSI/VT coloring, extended Unicode characters, pseudo-pixels (such as Unicode 13.0 sextants and Unicode 16.0 octants), and [Sixels](https://en.wikipedia.org/wiki/Sixel).



## Characters in this repository


### alexkidd
![alexkidd](images/alexkidd.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the Mark III / Master System game Alex Kidd in Miracle World / アレックスキッドのミラクルワールド.


### clippit
![clippit](images/clippit.png)

This uses MS-DOS codepage 437 characters and ANSI/VT colors (16 colors) and attributes.
It is based on the assistant from Microsoft Office.


### sxl-cow
![sxl-cow](images/sxl-cow.png)

This uses a sixel image.
It is based on the cow sprite from the Super Famicom / SNES game Earthworm Jim.

The idea of this character is to provide a "HD remaster" of the original cow.
It can be used as a replacement for the ANSI-art cow used when `cowsay` is called without a `-f` option. To achieve this, rename the `default.cow` that ships with cowsay to `legacy-cow.cow`, and create a symbolic link `default.cow` pointing to `sxl-cow.cow` as follows:
```bash
cd /usr/share/cowsay/cows
sudo mv default.cow legacy-cow.cow
sudo ln -s sxl-cow.cow default.cow
```


### dukenukem
![dukenukem](images/dukenukem.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the original PC game Duke Nukem by Apogee Software.


### flappybird
![flappybird](images/flappybird.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the mobile phone game Flappy Bird.


### sxl-guybrush
![sxl-guybrush](images/sxl-guybrush.png)

This is a sixel image conversion of Guybrush Threepwood from The Secret of Monkey Island.


### hellokitty
![hellokitty](images/hellokitty.png)

This uses extended Unicode characters and ANSI/VT colors (16 colors) and attributes (strikethrough, underline).
It is based on the Hello Kitty / ハロー・キティ character by Yuko Shimizu / Sanrio.


### sxl-indy
![sxl-indy](images/sxl-indy.png)

This is a sixel image conversion of Indiana Jones (Indy) from Indiana Jones and the Fate of Atlantis.


### link
![link](images/link.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is based on the Famicom / NES game The legend of Zelda / ゼルダの伝説 (The Hyrule Fantasy).


### link-16bit
![link-16bit](images/link-16bit.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the Super Famicom / SNES game The legend of Zelda / ゼルダの伝説 - A Link to the Past / 神々のトライフォース.


### mario
![mario](images/mario.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the Famicom / NES game Super Mario Bros, but with modern colors.


### sxl-mario+yoshi
![sxl-mario+yoshi](images/sxl-mario+yoshi.png)

This is a sixel image conversion of the Super Mario World sprites of Mario and Yoshi.


### mona
![mona](images/mona.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is based on the GitHub octocat mascot loading animation.


### ralph-face
![ralph-face](images/ralph-face.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is based on the cover of the movie soundtrack of Wreck-It Ralph.


### rover
![rover](images/rover.png)

This uses MS-DOS codepage 437 characters and ANSI/VT colors (16 colors) and attributes.
It is based on the assistant from Microsoft Bob and Windows XP.


### sxl-ryu
![sxl-ryu](images/sxl-ryu.png)

This is a sixel image conversion of a Ryu sprite from the game Street Fighter II.


### sxl-scrooge-face
![sxl-scrooge-face](images/sxl-scrooge-face.png)

This is a sixel image conversion of Scrooge McDuck's face from the DuckTales Famicom / NES game title screen.


### sxl-shadowdancer
![sxl-shadowdancer](images/sxl-shadowdancer.png)

This is a sixel image conversion of the main character and his dog sprites from Shadow Dancer / 影の舞.


### shinobi
![shinobi](images/shinobi.png)

This uses Unicode 13.0 sextants and ANSI/VT colors (256 colors).
It is based on the sprite of Joe Musashi in the Game Gear game The GG 忍 Shinobi.


### sonic
![sonic](images/sonic.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is based on the Game Gear version of the game Sonic the Hedgehog 2.


### sxl-strider
![sxl-strider](images/sxl-strider.png)

This is a sixel image conversion of Strider Hiryu / ストライダー飛竜 sprite from the eponymous game.


### tamagotchi
![tamagotchi](images/tamagotchi.png)

This uses Unicode 16.0 separated sextants.
It is based on the 1<sup>st</sup> generation of Tamagotchi / たまごっち LCD toy by Bandai.


### sxl-tentacle
![sxl-tentacle](images/sxl-tentacle.png)

This is a sixel image conversion of the Purple Tentacle sprite from Day of the Tentacle.


### tiki
![tiki](images/tiki.png)

This uses Unicode 16.0 octants and ANSI/VT colors (256 colors).
It is based on the arcade game The NewZealand Story.


### sxl-vanellope
![sxl-vanellope](images/sxl-vanellope.png)

This is a sixel image conversion of Vanellope von Schweetz character illustration from Wreck-It Ralph.



## Installing & using cow files
You'll need the cowsay utility, so start with `sudo apt install cowsay` or equivalent for your distro.

Copy the files from this repo's `cows` folder to  `/usr/share/cowsay/cows`.

Then simply use the `cowsay -f [character name] [message]` command.

For Unicode sextants and octants, you will need recent fonts that include the _Legacy Computing Symbols_, such as [Cascadia Mono](https://github.com/microsoft/cascadia-code) or [Iosevka Term](https://github.com/be5invis/Iosevka).
For sixels images support, [Windows Terminal](https://github.com/microsoft/terminal) or another VT340-compatible terminal emulator is required.

---

-- Philippe Majerus, September 2024

_These are all designed to celebrate classic pixel art nostalgia. All characters and trademarks are the property of their respective owners._

---

If you enjoy ANSI-art and Unicode semigraphics, also check out [my FIGfonts collection](https://github.com/PhMajerus/FIGfonts) and [my ANSI-art collection](https://github.com/PhMajerus/ANSI-art).
