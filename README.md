<p align="center">
  <img width="500" align="center" src="DETUTILS.png">
</p>
<h2 align = "center">Welcome to the <b>DETUtils</b> Wiki</h2>
<h4 align = "center">
  Addition to the Pawn language features, open.mp API and Discord Connector plugin.
</h4>

### Current library version: `2.0.7-R3`

Hello scripter! Welcome to *DEntisT's Utilities* (or **DETUtils** for short) "read me" file. So, now, you may ask about - what's this? Well - in general, this addition to open.mp Standard Scripting package contains libraries that have in-game visible effects and libraries that contain new scripting features. 
- Below, you can find information about each library.
- For better understanding of this, make sure you know Pawn and a_samp - read all the docs [here](https://team.sa-mp.com/wiki-archive.html)...

## Examples
Honestly, this package of libraries exists for show-off reasons, I made it for my own satisfication since I have a really big desire to code. You can still contribute and use it though. Example code:
- [View code](https://github.com/DEntis-T/SA-MP-DETUtils/blob/master/DETUTILS/d_testing/d_testing_internal.inc)

--------------------------------------

## Installation
- Installation is simple, quick and easy - learn more [here](docs/d_installation.md)...

## Documentation
Below is a list of all the libraries provided by the DETUtils package. They're all optional unless they're used internally, in that case you'll get a warning.

| Library      | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
| [detutils.inc](docs/detutils.md) | Entry point from which everything is included. |

### Pawn/Coding Libraries (`13`)
Libraries whose contain the new language features.

| Library      | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
| [d_vars.inc](docs/d_vars.md) | A library which reserves up space for new variables you can dynamically allocate during run-time, which is really similar to `malloc` but can handle up to hundreds of variables, stacks and arrays of different types. |
| [d_als.inc](docs/d_als.md) | New ALS hooking system. |
| [d_foreach.inc](docs/d_foreach.md) | New `foreach` implementation. |
| [d_tables.inc](docs/d_tables.md) | Excel-like table management system. |
| [d_profile.inc](docs/d_profile.md) | Profile chunks of code and see how much does it take to execute it. |
| [d_timers.inc](docs/d_timers.md) | A replacement for `SetTimer(Ex)` which now adds both automatic and manual timers (automatic timers defer themself on the script initialization). |
| [d_events.inc](docs/d_events.md) | A replacement for `Call<Local/Remote>Function` and `forward`/`public` which gives you more possibilities and automations, such as local and global functions (on file level), command events, property events and dialog events (extensions of DETUtils API itself). |
| [d_fmargs.inc](docs/d_fmargs.md) | A rewrite of `y_va` and Pawn `sscanf` implementation. |
| [d_testing.inc](docs/d_testing.md) | Provides fast and easy way of testing. |
| [d_global.inc](docs/d_global.md) | A library which makes expressions possible on the global level - or in simple terms, code outside other functions. |
| [d_ascii.inc](docs/d_ascii.md) | ASCII character predefines. |
| [d_core.inc](docs/d_core.md) | The folder containing all the libraries used by the DETUtils system itself. |
| [d_lambda.inc](docs/d_lambda.md) | Provides new small lambda functions. |

### SA:MP Libraries (`10`)
Libraries whose contain the new SA:MP functions and features.

| Library      | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
| [d_permissions.inc](docs/d_permissions.md)  | Edit player SA:MP server permissions. |
| [d_commands.inc](docs/d_commands.md) | Command processor with a big amount of features. |
| [d_properties.inc](docs/d_properties.md) | Create property entrances, with own and custom interiors. |
| [d_visual.inc](docs/d_visual.md) | Generally smaller groups of random visual features. |
| [d_anticheat.inc](docs/d_anticheat.md) | Anti cheat system. |
| [d_mapeditor.inc](docs/d_mapeditor.md) | In-game map editor. |
| [d_factions.inc](docs/d_factions.md) | Player factions (groups of players) made easy. |
| [d_dialog.inc](docs/d_dialog.md) | A replacement `ShowPlayerDialog` and `OnDialogResponse` containing even more callbacks and functions to manipulate dialogs. |
| [d_server.inc](docs/d_server.md) | Generally server-related functions. |
| [d_races.inc](docs/d_races.md) | A racing system with many features. |
| [d_editobject.inc](docs/d_editobject.md) | New `EditObject()`/`EditPlayerObject()` system with many more features. |

### Discord API Libraries (`1`)
Libraries whose contain the new functions for Discord bot development - these are extensions to Discord Connector plugin and they require the plugin to work.

| Library      | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
| [d_discordapi.inc](docs/d_discordapi.md) | Addition to the Discord Connector plugin. |

### Storage Libraries (`3`)
Libraries whose provide storing (saving), loading and managing persistent data on your server.

| Library      | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
| [d_filequeries.inc](docs/d_filequeries.md) | Send file queries, save and load cache during runtime. |
| [d_toml.inc](docs/d_toml.md) | Save, load and manage TOML files. |
| [d_yaml.inc](docs/d_yaml.md) | Save, load and manage YAML files. |

--------------------------------------

Documentation contains some extra notes and tips.

- Read more here: [Extra stuff](docs/d_extra.md)
## Tests
- I regularly make test scripts with all new features I added to the library to ensure everything is working as expected. If not, I write it down in to a test log.

Check out test script here:

- [Go to tests...](docs/d_testscript.md)

- You can also run **DETUtils** test script directly from your includes, just use the definition below before including the libraries.
```pawn
#define DETUTILS_TESTING_MODE
```
> As I mentioned, `DETUTILS_TESTING_MODE` flag will enable the test script automatically.

## Test artifacts
- You can go to [GitHub Actions](https://github.com/samp-api/DETUtils/actions) page for this repository, select the latest workflow run from the list and download the **sampctl** auto-build artifact.

## Filterscripts
- If you're making a filterscript using the *DETUtils* includes, make sure to enable the `DETUTILS_FILTERSCRIPT_MODE` flag.

```pawn
#define DETUTILS_FILTERSCRIPT_MODE
```

- It'll also work if you just simply do:

```pawn
#define FILTERSCRIPT
```

## Limits

- Everything has its limits, so does DETUtils - view them [here](docs/d_limits.md)...

## Beta testing

- Beta testing program is currently down since this project is far away from being done. Also, according to news - new **open.mp** is coming soon, so these libraries shall be updated regularly to keep up with the project.

## Test log

- Recently, I started test logging program in which I log every library issue I spotted during testing. You can check it [here](docs/d_testlog.md)...

## Versioning

- Read more about DETUtils versioning system [here](docs/d_versioning.md)...

## More languages

- English isn't the only language on the planet though, that's why I started language contribution program. I started it by making another library's core include called **d_text.inc** in which are all strings located. Your job as a language contributor is to simply translate it!

Check the file [here...](DETUTILS/d_extra/d_text.inc)

## Troubleshooting

If you're facing unusual problems, that aren't supposed to be here or were not happening ever before, or they magically appeared after the update - make sure you enable automatic debugging.
- Automatic debugging literally sends debug messages whenever it needs to.
- With this feature you can easily track problems and report them on Discord or try to troubleshoot them yourself.

To enable advanced debugging feature, use:

```pawn
#define DETUTILS_DEBUG_MODE
```

To join Discord server, [click this link!](https://discord.gg/samp)

**NOTE:** After you enabled advanced debugging, your console may be full with *DETUtils* debug messages - in that case, don't worry.

## Compile-time issues

If you're facing issues with your code compilation after including the library, make sure you have updated Pawn Compiler and SA:MP Standard library package and libraries. Using them outdated can indeed cause issues while trying to implement newer libraries to your code.

- You can get the latest version of SA:MP standard libraries [here](https://github.com/pawn-lang/samp-stdlib)...

- You can get the latest version of Pawn standard libraries [here](https://github.com/pawn-lang/pawn-stdlib)...

- You can get the latest version of Pawn Compiler for SA:MP [here](https://github.com/pawn-lang/compiler/releases)...

## DEntisT's Utilities

### Legal:

- Read the license [here](license.md).

### Other contributors:

- No one yet.

### Thanks to these people for:

- aezzakmi (no GitHub account) - really productive testing
- [Y_Less](https://github.com/y-less) & Zeex - fmargs ``#emit`` stuff, d_commands decorator concept
- [Zeex](https://github.com/zeex) - ZCMD command processor concept
- Y_Less - code parser, another amazing thing which you can get [here](https://github.com/y-less/code-parse.inc)
- Kirima - command guesser, another cool thing you can get [here](https://github.com/se8870/samp-command-guess)
- Zeex - AMX assembly

### Contributions

- Just fork the repository, apply your wanted changes and create a pull request!
