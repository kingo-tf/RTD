> * [Discord](https://discord.gg/sUgJE278QS)
> * [AlliedModders Thread](https://forums.alliedmods.net/showthread.php?t=278579)
> * [Balance Spreadsheet](https://docs.google.com/spreadsheets/d/1LH_-Lk5Uho-i_rpefjpn4mBGlLWrel_5rsBtLC-RVvs/edit?usp=sharing)
> * [Perk List](https://github.com/Phil25/RTD/wiki/perk-list)
> * [Commands](https://github.com/Phil25/RTD/wiki/commands)
> * [ConVars](https://github.com/Phil25/RTD/wiki/convars)
> * [Customizing Perks](https://github.com/Phil25/RTD/wiki/customizing-perks)
> * [Changelog](https://github.com/Phil25/RTD/wiki/changelog)
> * [API Documentation](https://github.com/Phil25/RTD/wiki/api-documentation)

# About this fork

This is a fork of [Phil25/RTD](https://github.com/Phil25/RTD) for TF2 Rebalanced servers (game folder `tf_ktbm`) running the [kingo-tf/sourcemod](https://github.com/kingo-tf/sourcemod) build. The links above and the rest of this README describe the original plugin. For regular Team Fortress 2 servers, use the original.

Differences from the original:
* **[tf2attributes](https://github.com/FlaminSarge/tf2attributes) is not used.** Attributes are set through the `TF2R_*` natives of the `game.tf2r.ext` extension (`tf2r_attributes.inc`). The plugin does not load without that extension.
* The plugin also loads when the game folder is `tf_ktbm`, not only `tf`.
* The source compiles with the SourcePawn 1.13 compiler.
* Updater, if compiled in, reads `update.txt` from this fork instead of the original.

## Compiling

Use `spcomp` from SourceMod 1.13 and add the `plugins/include` directory of kingo-tf/sourcemod to the include path, since it provides `tf2r_attributes.inc`:

```
cd scripting
spcomp rtd.sp -i <path to kingo-tf/sourcemod>/plugins/include -o ../plugins/rtd.smx
```

The `spcomp.exe` and build scripts in `scripting/` come from the original repository and do not know about that include path.

# Roll The Dice Revamped

Roll The Dice mod for Team Fortress 2. It allows players to "roll the dice" for one of 82 random effects, some good, some bad. The effect will be applied for its custom time to the player and removed afterwards.

Roll The Dice Revamped is a rewrite of [pheadxdll's Roll The Dice](https://forums.alliedmods.net/showthread.php?p=666222) with numerous features added, most notable of which are listed here:
* **[Requires SourceMod 1.11 or higher](http://www.sourcemod.net/downloads.php?branch=stable)**.
* 48 new perks added, making up a total of 82 perks.
* (for devs) An easy way of adding completely custom perks.
* Fixed some overpowered/broken effects.
* Highly customizable config, with different settings for nearly each effect.
* Added `sm_rtd` command for rolling, bindable for players.
* Added `sm_removertd` command to force remove perks from anyone.
* Improved `sm_forcertd` to include custom time.
* HUD-based timer display, with ConVar-adjustable position.
* Limiting any perk to any class(es).
* Setting custom initiation sound of any perk.
* Setting custom time of any perk.
* Possibility to interchange perks' call functions.
* Built-in effect search-up, with custom output format option.
* Improved perk addressing, with support for adding custom target strings.
* The original version's _Legacy_ mode can be limited to a number of players.
* Setting how many times a perk is not allowed to repeat per player/globally.
* Improved the rolling algorithm.
* (for devs) More advanced and fixed include file.
* (for devs) Written in the new syntax.
* More flexible way of disabling perks.
* Other plugins can add their own perks and handle their effect themselves.
* Other plugins can override an effect of any perk.
* [Updater](https://forums.alliedmods.net/showthread.php?t=169095) support.

## Installation instructions or discussion → [Allied Modders Thread](https://forums.alliedmods.net/showthread.php?t=278579)
## Bug reporting or feature requests → [GitHub's Issue Tracker](https://github.com/Phil25/RTD/issues)
