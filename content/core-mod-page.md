# Fish Farm Festival Core

**The content engine behind the Fish Farm Festival modpack**: seasonal festivals, skill-tree content, food buffs, a year-round market, bounties and adventure loot that ties fishing, farming and cooking together.

This is a **data-only** Fabric mod for Minecraft 1.20.1. It adds no new blocks or items and contains no code. It uses datapack content, such as functions, advancements, loot tables, tags, worldgen overrides and compatibility files, to connect the mods listed below into one gameplay loop.

## What it adds

### 🎉 Seasonal festivals (Serene Seasons)
- Four 16-day festivals follow the season calendar: **Blossom Fair** (spring), **Grand Fishing Derby** (summer), **Harvest Feast** (autumn) and **Christmas** (winter).
- A festival merchant comes to the player, who can trade seasonal crops, fish and dishes for **Festival Tokens**.
- Each merchant also has themed goods and rare *Festival Treasure* deals.
- Christmas adds Santa, an elf helper, snow on Christmas Eve and a gift on Christmas morning.

### 🌳 Skill-tree content (Pufferfish's Skills)
- **Angler**, **Farmer** and **Chef** perks.
- Discovery XP for new fish, crops and dishes.
- Harvest Crates from Farmer XP.
- Mastery Crates once a tree is complete.

### 🍲 Food buffs
- Every mod dish gives a buff based on its type: seafood, hearty, sweet or feast.
- Harder recipes give longer buffs.

### 🛒 Town Market (Farming for Blockheads)
- Emerald shop entries for:
  - seeds and saplings
  - animals
  - fishing and aquarium gear
  - kitchen tools
  - building blocks
  - boats
  - enchanted books

### ⚔️ Adventure loot
- Illager Invasion mobs appear in illager structures and on the Illager Warship.
- Tougher illagers drop special **Tide baits**, rare seeds and tokens.
- Dungeons & Taverns chests can contain bonus loot.

### 📜 Bounties, villagers and guide
- Bounty decrees for Angler, Farmer, Chef and Town Guard (Bountiful).
- Fisherman and farmer trades for Villagers Plus.
- An **FFF Journey** advancement tab that guides new players.

### 🌱 Worldgen tweaks
- Mod crops, grape bushes and most mod fruit trees no longer generate in the wild, so seeds become something you earn.
- Vanilla plants and coconut palms still generate.

## Required mods
Tide, Pufferfish's Skills, Farmer's Delight Refabricated, [Let's Do] Farm & Charm, [Let's Do] Vinery, [Let's Do] Brewery, Expanded Delight, Snowy Spirit, Bountiful, Farming for Blockheads, Serene Seasons, Hybrid Aquatic, Illager Invasion and Illager Warship.

## Recommended mods
Macaw's Holidays, Macaw's Lights, Hearth & Home, Ocean's Delight, Ecologics, Dungeons and Taverns, Villagers Plus, Dusty Decorations, Better Fishtanks, Small Ships, Comforts and Backpacked.

## Notes
- Built for the **Fish Farm Festival** modpack, which also ships the skill-tree layouts in its config. The mod works with the required mods above, but it is balanced for the pack.
- The mod id is `zz_fishfarmfestival` on purpose. Fabric loads mod data in alphabetical order by mod id, so this id makes the worldgen tweaks load after the mods they change.
