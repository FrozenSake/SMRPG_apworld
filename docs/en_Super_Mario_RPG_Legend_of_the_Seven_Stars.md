# Super Mario RPG: Legend of the Seven Stars (SNES)

## Where is the settings page?

Currently there isn't one. In the future the [player settings page for this game](../player-settings) should contain all the options you need to configure and export a
config file.

## Okay, how do I get set up then?

### Requirements for everyone:

1. Archipelago is set up correctly, see [this guide](https://archipelago.gg/tutorial/Archipelago/setup/en#installing-the-archipelago-software)

### For Archipelago Host

#### Requirements
1. Latest APWorld from [here](https://github.com/TheRealSolidusSnake/SMRPG_apworld/releases)
    - Don't forget to add it to your archipelago setup
2. Have an SMRPG US ROM in an easy to locate place 

#### Hosting

Beyond this, generate the archipelago seed as normal. That means putting YAMLs in players, getting the output in output, etc. etc. - [this guide](https://archipelago.gg/tutorial/Archipelago/setup/en#generating-a-multiplayer-game) covers this, and you should be comfortable with doing this for the base games before trying to play with this nonsense.

### For the SMRPG Player(s)

1. [Bizhawk](https://github.com/TASEmulators/BizHawk/releases) - installation guide [here](https://github.com/TASEmulators/BizHawk?tab=readme-ov-file#installing)
2. The same things the host needs:
    - Latest APWorld from [here](https://github.com/TheRealSolidusSnake/SMRPG_apworld/releases)
    - Have an SMRPG US ROM in an easy to locate place 
3. A YAML ready to go, see the [YAML Section](#making-your-yaml)
4. Give the YAML to your host, of it you're self-hosting, scroll back up to the [hosting section.](#hosting)
5. Receive the `.apsmrpg` file from your host (or grab it from the zip in the output file if you're hosting)
6. Run it...
    - If you've already associated this filetype with Archipelago, you're going to just get where you're going
    - If you haven't select `ArchipelagoSNIClient.exe` from the Archipelago install folder
7. Enable the SNI Connector LUA from `PATH/TO/archipelago/SNI/lua/Connector.lua`
    - The safest and easiest way to do this is to drag the `.lua` file on to bizhawk

#### Making your YAML

1. Grab the YAML from the this Repository's releases section then do your options
    - At the bare minimum, set the `name:` field to something usable and distinct.
2. Change any other options as you see fit.
    - Definitely review them, the defaults may not be to your liking.

## What does randomization do to this game?

All acquirable pickups are shuffled among each other. Logic is in place to ensure that the game is always completable.

The whole world map is open, although entry into Bowser's keep may be locked behind stars, depending on your settings.
Shops generally are restricted to certain types of items, but those items are shuffled.

## What items and locations get shuffled?

In general, all item pickups in the game. More formally:
- Stuff, things, and placeholder text.

## What items from The Legend of Zelda can appear in other players' worlds?

All items can appear in other players' worlds. "You Missed" does not function as a funny trap if it's not found locally.

## What does another world's item look like in SMRPG?

Since all items are obtained from battles or chests, they are not distinguishable.

## Are there any other changes made?

- The full map is available from the start.
- You can start with either 1 or 3 party members.
    - If you start with 3, the following locations unlock new members: `Forest Maze`, and `Marrymore`
    - If you start with 1, it will be the above, plus: `Mushroom Way`, and `Moleville`
