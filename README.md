# SkyData

A Paper/Spigot 1.16.5 plugin that records ShopGUI+ buy/sell transactions and shows them in a sortable in-game menu.

## Features

- Listens to ShopGUI+ transaction events and stores the data
- `/skydata` menu listing items, sortable by amount sold or bought
- Menu text and buttons configurable in `config.yml`

## Tech stack

- Java 11, Maven
- Paper API 1.16.5, ShopGUI+ API, SmartInvs

## Getting started

Requirements: JDK 11, Maven, and `spigot-1.16.5.jar` placed in `lib/` (not committed; build it with [BuildTools](https://www.spigotmc.org/wiki/buildtools/)).

```bash
mvn package
```

Copy the jar from `target/` into the server's `plugins/` folder. ShopGUI+ must be installed on the server.

## Commands

| Command | Description |
|---|---|
| `/skydata` | Open the transaction data menu |

## Project structure

```
src/main/java/com/emre/skydata/
├── DataMain.java       # plugin entry point
├── DataListener.java   # ShopGUI+ transaction listener
├── DataManager.java    # data storage
├── DataMenu.java       # GUI
└── utils/
```

## License

[Apache License 2.0](LICENSE.md)
