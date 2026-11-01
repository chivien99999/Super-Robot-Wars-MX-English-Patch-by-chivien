# Super Robot Wars MX Portable - English Patch (v0.2 playtest)

This is my English translation patch for **Super Robot Taisen MX Portable** (PSP, ULJS-00041).

> **Early playtest.** Version 0.2 is an early playtest build. There has been no full playthrough yet, so expect bugs, odd line breaks and lines that still need polish. Please report anything you find (see below).

## What's new in v0.2

- **New font.** I redrew the English font as a crisp 1-pixel bitmap font with the same soft grey shading as the original Japanese font. Every letter is the same width as in v0.1 or narrower, so no line got longer. I hand-fixed the digits and the letters that looked wrong at this size.
- **Round brackets.** ( ) are now properly curved, so "(100)" no longer reads like "[100]". Brackets around numbers use the same font as the numbers.
- **Numbers line up.** A "---" is now exactly as wide as a 3-digit number, so dashes and numbers sit in the same column (Raise Stats, Weapon Performance, Pilot Status skill levels, Parts).
- **Smooth opening narration.** The scrolling text at the start of the game now scrolls smoothly, with every line moving together and even gaps between lines.
- **Aligned footer keys.** The two words in each column of the button key along the bottom of the screen (for example Attribute / Field, W Attack / Guided) now start at the same spot.
- **Menu fit fixes.** Swap Main Pilot: each Spirit's SP cost sits right after its own name. Swap Pilots: long skill names stay inside the frame. Parts descriptions wrap cleanly and no longer mix two font sizes.
- **Script fixes.** I re-broke 23 story pages at natural points so they read better, and tidied the wording in one line.

## What I translated

- The full story script: every scene and intermission conversation
- Battle quotes for every pilot
- Menus, system messages and every in-game screen (intermission, map, pre-battle, unit and pilot status, sortie, shop, options, save/load)
- Unit, pilot, weapon, Spirit Command, skill and part names and descriptions
- Stage names and chapter title cards
- Text in the game's images: banners, command and status badges, headers, the shop sign, and the boot screens
- The title logo, plus the XMB icon and save icon
- Subtitles for the voiced cut-scenes, and the ending staff roll
- The name entry screens now use the English letter set

## Warnings

- **Early playtest:** nobody has played the game start to finish on this patch yet. Keep several save files.
- The patch only works on the original, unmodified Japanese ISO (see the checks under "How to apply"). A different or edited dump will be refused.
- Tested on PPSSPP. It has not been tested on real PSP hardware yet. On a real PSP you need custom firmware to run any ISO.
- Save states from other versions of the game (Japanese or an older build) may not carry over cleanly. Use in-game saves.
- This repository holds patch files only. It does not contain the game. You need your own copy.

## How to apply (Windows)

1. Download `SRW_MX_Portable_English_Patch_v0.2.zip` from the `playtest` folder.
2. Unzip it into the folder that holds your Japanese ISO (or into a folder inside it). The ISO must be named exactly:
   `Super_Robot_Taisen_MX_Portable_JPN_PSP-Caravan.iso`
3. Double-click `patch.bat`.
4. Wait for **DONE** (about a minute). The English ISO is written next to the Japanese one:
   `Super_Robot_Wars_MX_Portable_EN_v0.2.iso`

Your Japanese ISO is never changed. `patch.bat` checks both files for you:

| File | Size | MD5 |
|---|---|---|
| Japanese ISO (input) | 1,295,122,432 bytes | `448d168edcd3edfe62cdcb9b31c87820` |
| English ISO (output) | 1,357,854,720 bytes | `7998faa5e68f827c674686f1e6823536` |

**Other systems (Linux / macOS):** install xdelta3 and run

```
xdelta3 -d -s Super_Robot_Taisen_MX_Portable_JPN_PSP-Caravan.iso MX_EN_v0.2.xdelta Super_Robot_Wars_MX_Portable_EN_v0.2.iso
```

## Optional: PS2 balance add-on

### What it changes

When MX came to the PSP, the enemies got tougher than in the PS2 original: every enemy unit has 1.5 times its PS2 HP, and every unit pays out only 80% of its PS2 funds when you shoot it down. A lot of players dislike that change, so I made an optional add-on that puts the PS2 numbers back:

- **Enemy HP:** 139 enemy units go back to their PS2 HP (the PSP value divided by 1.5). For example, the Galfa Emperor goes from 285,000 back to 190,000, the final Devil Gundam from 225,000 to 150,000, and AI1 from 600,000 to 400,000.
- **Funds:** all 295 units go back to the PS2 funds they pay out when shot down (the PSP value divided by 0.8). For example, a unit worth 1,200 on the PSP is worth 1,500 again.

That's all it changes. The translation, the game program and everything else stay exactly the same as the main patch. I only compared the unit data and the stage files with the PS2 disc. Enemy placements and levels on the maps are already the same as the PS2 version, so the HP and funds were the whole rebalance.

What it does **not** change (these stay as the PSP has them):

- The +200 Armor the PSP gave six G Gundam Super/Hyper Modes (Gundam Maxter, Gundam Rose, God Gundam (also while mounted), Dragon Gundam and Bolt Gundam)
- The PSP's new and rewritten scenes, and the few small stage tweaks that came with them

### How it works

The add-on is a second, small patch that goes on top of the English ISO. It never touches your Japanese ISO or your English ISO. It writes a third ISO, so you can keep both versions and pick either one.

1. Make the English ISO first (steps above).
2. Unzip `SRW_MX_Portable_PS2_Balance_Addon_v0.2.zip` into the folder that holds the English ISO.
3. Double-click `patch.bat` and wait for **DONE**. The new file is written next to it:
   `Super_Robot_Wars_MX_Portable_EN_v0.2_PS2_balance.iso`

`patch.bat` checks that the input is the exact English v0.2 ISO, and it checks the result too:

| File | Size | MD5 |
|---|---|---|
| English ISO (input) | 1,357,854,720 bytes | `7998faa5e68f827c674686f1e6823536` |
| PS2 balance ISO (output) | 1,357,854,720 bytes | `397fcfbce3bc57e2940ed5d2725e8f4c` |

Other systems:

```
xdelta3 -d -s Super_Robot_Wars_MX_Portable_EN_v0.2.iso MX_EN_v0.2_PS2_balance.xdelta Super_Robot_Wars_MX_Portable_EN_v0.2_PS2_balance.iso
```

## Bug reports

Please report bugs, typos and anything that looks wrong on my Discord server: https://discord.gg/euYRPdJf69

A screenshot and where it happened (stage or scene) helps me a lot.

## Credits

- redditusernameunavailable on Discord

The patcher uses xdelta 3.1.0 (https://github.com/jmacd/xdelta-gpl).
