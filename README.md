# ZianOBS

ZianOBS is a small, non-invasive runtime diagnostic mod for Minecraft 1.21.1 + NeoForge + Cobblemon 1.8.1.

It observes Cobblemon spawn-related event paths and writes structured `[ZIAN-OBS]` lines to the server log. It is intended for development, compatibility testing and incident diagnosis.

## Safety contract

ZianOBS is observer-only. It must not cancel Cobblemon events, mutate spawn actions, modify Pokémon, remove entities, or alter game state.

## Observed paths

- final entity spawn events
- Pokémon entity spawn events
- fishing Pokémon pre/post events
- Poké Snack pre/post events
- activated Habitat events
- party send-out events
- Pokémon entity load events

## Target

Minecraft 1.21.1 · Java 21 · NeoForge 21.1.251 · Cobblemon 1.8.1.

Youer 1.21.1 is a compatibility test target after the NeoForge baseline.

## Logs

Filter `latest.log` for `[ZIAN-OBS]`.

## Build

```bash
gradle --no-daemon build
```

GitHub Actions builds the project and publishes the JAR as `zianobs-neoforge-1.21.1`.

## Status

Research/diagnostic utility. It is not a gameplay mod or enforcement layer.

## License

MIT. See [LICENSE](LICENSE).
