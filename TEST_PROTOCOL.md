# ZianOBS runtime test protocol

## Natural spawning
Start NeoForge + Cobblemon + ZianOBS, wait for normal Pokémon spawning and capture all `[ZIAN-OBS]` lines. Record spawner and cause classes.

## Fishing
Correlate `FISHING_PRE`, `POKEMON_ENTITY_SPAWN`, and `FISHING_POST` using SpawnAction identity and the final Pokémon UUID.

For a canceled fishing spawn, record whether `FISHING_PRE canceled=true` appears and whether `FISHING_POST` is absent. Also record the visible bobber behavior in-game. This is useful when diagnosing a fishing flow that does not terminate after cancellation.

## Poké Snack
Correlate `POKE_SNACK_PRE`, `POKEMON_ENTITY_SPAWN`, and `POKE_SNACK_POST`.

## Activated Habitat
Trigger repeated activated Habitat spawns and record `HABITAT_ACTIVATED` plus subsequent final Pokémon spawn events. Do not infer causation from a single run.

## Party send-out
Send out a party Pokémon and inspect `POKEMON_SENT_POST finalSpawnSeen=...`.

## Existing entity load
Persist Pokémon entities, restart, then compare `POKEMON_ENTITY_LOAD` with any final spawn records.

## Report fields
```text
test id
date
Minecraft
NeoForge/Youer
Cobblemon
ZianOBS commit
other mods/addons
steps
relevant [ZIAN-OBS] lines
result
interpretation
needs repeat
```
