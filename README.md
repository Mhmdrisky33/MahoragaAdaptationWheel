# Mahoraga's Adaptation Wheel (NeoForge 1.21.1)

Target: Minecraft Java 1.21.1, NeoForge 21.1.251+; Java 21.

## Alpha features in this source project
- Craftable `Roda Adaptasi Mahoraga` item (also available in the Tools & Utilities creative tab).
- Right-click the item to activate/deactivate adaptation.
- A low-poly gold wheel item model is rendered above the local player's head while active, with a slow spin animation.
- Damage message IDs are tracked separately. Each new hit adds 20% progress. At 100%, later damage of that same type is reduced to 25% of normal damage.
- Progress and active state are saved in the player's persistent data.
- Press **O** to open the adaptation panel. Progress is synchronized from server to the owning client.
- Includes an original synthesized metallic ratchet/spin sound.

## Crafting
`G = Gold Ingot`, `A = Amethyst Shard`, `E = Ender Eye`

```
G A G
A E A
G A G
```

## Build on GitHub (recommended if you only have a phone)
This project includes a GitHub Actions workflow at `.github/workflows/build.yml`.

1. Create a new repository on GitHub and upload the contents of this project (the folder containing `build.gradle`, `settings.gradle`, and `src`).
2. Open the repository's **Actions** tab.
3. Select **Build NeoForge mod** and press **Run workflow** (or push the files to `main`).
4. Wait for the workflow to finish. Open the completed run and download the artifact named `MahoragaAdaptationWheel-NeoForge-1.21.1`.
5. Extract the artifact ZIP. Put the `.jar` inside your Minecraft 1.21.1 NeoForge profile's `mods` folder.

The GitHub workflow uses Java 21 and Gradle 8.12, then runs `gradle build` against NeoForge 21.1.251.

## Important alpha limitations
- This source has not yet been compiled or launched in Minecraft. A successful GitHub Actions build is still required before installing it.
- The wheel is currently rendered for the local player only; multiplayer visibility for other clients and in-game visual/audio tuning need runtime testing.
- The current adaptation system reduces matching damage after the adaptation reaches 100%; it does not grant immunity.
- Mobile launchers such as Zalith need the built `.jar`, not this source ZIP.
