# COREBOUND: Descent to the Center

## Overview
Corebound is a Roblox mining adventure set on a mysterious, procedurally-generated planet. Players descend through layers of terrain to discover rare ores, craft advanced equipment, and uncover the secrets of an ancient civilization hidden near the planet's core.

## Core Gameplay Loop
1. **Mine Resources** – Use pickaxes, drills, explosives, and other tools to break through blocks and collect ores.
2. **Process & Trade** – Sell raw materials for quick cash or refine them at forge stations to create higher-value components.
3. **Upgrade & Craft** – Spend earnings on improved tools, exosuits, jetpacks, and support gadgets like scanners or mining drones.
4. **Descend Deeper** – Unlock new biomes every 1,000 meters with unique hazards, physics, and loot tables.
5. **Uncover Lore** – Discover data logs and artifacts from Eclipse Corp., piecing together the planet's past.

## Key Features
- **Layered Biomes** – Distinct environmental zones such as Verdant Stonefield, Amber Caves, Magma Hollows, Obsidian Abyss, and the Ancient Core.
- **Dynamic Challenges** – Shifting gravity, temperature extremes, low visibility, and energy storms add variety to each descent.
- **Automation & Co-op** – Deploy mining drones for passive gathering and form Mining Guilds to share dig sites, storage, and teleporter networks.
- **Economic Depth** – Participate in a fluctuating ore market, refine resources into high-value goods, and trade blueprints via an auction house.
- **Base Building** – Establish underground bases with oxygen generators, storage vaults, refineries, and decorative elements.
- **Narrative Progression** – Collect relics to assemble the Core Stabilizer, determining the planet's fate through branching endgame choices.

## Monetization Ideas
- Gamepasses for quality-of-life upgrades such as Auto-Drill Drones, Backpack Expanders, Ore Scanners, and Night Vision Helmets.
- Cosmetic bundles featuring holographic pets, jetpack skins, and animated pickaxe trails.

## Technical Considerations
- Procedural terrain using seeded chunks for replayability across servers.
- Persistent data tracking depth, equipment, bases, and guild memberships.
- Optional first-person mode with dynamic lighting sourced from player gear.

## Playable Prototype

A functional prototype of Corebound is provided in [`CoreboundStarter.rbxmx`](./CoreboundStarter.rbxmx). Import the model into a Roblox Studio place to explore a simplified version of the gameplay loop:

- Procedurally populates a multi-layer mine with ores that respawn after a short delay.
- Awards credits and tracks maximum depth for each player.
- Provides two starter tools (a pickaxe and an amber drill) with different mining speeds.
- Automatically creates a HUD that displays credits, depth, and ore inventory counts.

### How to install in Roblox Studio

1. Download `CoreboundStarter.rbxmx` and import it into your place (e.g., **Model → Import**).
2. After the model appears in the Workspace, run the experience once. The included installer script moves every asset into the appropriate service (ServerScriptService, ServerStorage, StarterPlayer, etc.) and then removes itself.
3. Press **Play** in Studio to test. You will spawn with starter tools and can begin mining the generated cavern.

### Extending the prototype

- Add new tools by duplicating an existing tool inside `ServerStorage/CoreboundTools` and updating the stats in `ServerScriptService/Corebound/ToolStats`.
- Adjust generation parameters such as block size, layer size, and ore rarity in `ServerScriptService/Corebound/MineConfig`.
- Expand the HUD or create new UIs by editing the `CoreboundHUD` LocalScript in `StarterPlayerScripts`.
- Introduce selling stations, quest givers, or base-building systems by building on the server scripts inside `ServerScriptService/Corebound`.

## Future Expansions
- **Surface City** – A social hub with trading posts, mission boards, and PvP arenas.
- **Void Layer** – A secret endgame biome beneath the core featuring distorted gravity and alien ores.
- **Player Economy Enhancements** – Guild-owned territories and exclusive mineral rights to drive late-game competition.
