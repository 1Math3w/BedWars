# BedWars

Minecraft BedWars Spigot plugin made for server networks.

## Features

- All the basics of BedWars game (Teams, Resource spawners, etc.)
- Spectator mode
- Special items
- Resource spawners holograms
- Shop
    - Shift Click - Buys stack of that item
    - Dependent on player
        - Team colored blocks
        - Item color depends on whether player can afford that item (this data is real-time updated)
- Statistics can be stored in MySQL database
    - Win count `wins`
    - Draw count `draws`
    - Lose count `loses`
    - Current Win Streak  `win_streak`
    - Highest reached Win Streak `highest_streak`
    - Amount of kills `kills`
    - Amount of kills that eliminated player `final_kills`
    - Amount of kills that were first in that game`first_bloods`
    - Amount of deaths`deaths`
    - Amount of broken beds`bed_breaks`

## How To Use

This plugin follows the concept of 1 arena / server.

### Slime World Manager

- Maps are managed via SlimeWorldManager
- You have to create a map in a world generated by SWM, this plugin then clones the map and creates a temporary world
  called arena
- You have to use MySQL as a map storing system
- [How to use SWM](https://www.spigotmc.org/resources/slimeworldmanager.69974/)

### Setup

- Set maps locations inside `maps.yml`
- Set lobby locations inside `locations.yml`
- If you'd like to store statistics setup mysql database inside `mysql.yml`

### Customize

- There is no way to change UI, shop or any plugin functionality without modifying the source code, so if you'd like to
  customize the plugin, you have to fork.
- Default UI and shop were highly inspired by BedWars game at [QPlay.cz](https://qplay.cz)