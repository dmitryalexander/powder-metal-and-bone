# Powder, Metal & Bone

PMB is a Titanfall 1 mod for R1Delta private matches. Paragon starts as a pilot free-for-all and ends with a fight for the title. Hold the title for two minutes total to win. Your clock pauses when you lose the title and resumes when you take it back.

## Requirements and installation order

1. **Newest R1Delta required.** Install [R1Delta 3.0.5 Escrow 6](https://github.com/r1delta/r1delta/releases/tag/v3.0.5), the latest release when this build was packaged. This PMB package targets that exact version.
2. **Pilot Bots required.** Install [Pilot Bots 2.1.7](https://github.com/lcvb1997/R1Delta-PilotBots-Mod/releases/tag/Pilot-bots-v2.1.7) into the same R1Delta version. Use the original author's installer.
3. **Install PMB.** Download and extract the ZIP from [PMB releases](https://github.com/dmitryalexander/powder-metal-and-bone/releases). Close Titanfall and the launcher. Run the included installer against the R1Delta application folder and the Titanfall game folder.
4. **Katie's Reticle Mod is optional.** Install [Katie's Reticle Mod at the supported revision](https://github.com/KatDiedAgain/Kat-R1D-Mods/tree/4b3a530cd2f6bca040bbab463f8cf647d4d18041/Katies_Reticle_Mod) and apply the separate PMB compatibility ZIP from the release. Follow the instructions in that ZIP so Katie's sway fix and PMB's weapon settings work together.

**Frontier Overhaul is incompatible.** Disable it before running PMB.

## Install PMB

Open PowerShell in the extracted ZIP folder. Pass the folder that contains `Titanfall.exe` and its `r1delta` subfolder as `RuntimeRoot`. Pass the Titanfall content folder that contains `r1` and `vpk` as `GameRoot`.

```powershell
.\Install-PMB.ps1 -RuntimeRoot 'C:\path\to\R1Delta\app-3.0.5' -GameRoot 'C:\path\to\Titanfall'
```

Add `-CheckOnly` to check the files before installation. The installer checks the required versions and package files, saves replaced files to a backup folder, and reports its location. Restart R1Delta and enable **POWDER METAL & BONE** and **PMB.Continuous_Radar** in the Addons menu. Select **Private Match → Paragon**.

Use the same PMB and dependency versions on the host and each player's PC. This is a multiplayer preview. A full match with a remote second player still needs testing. Pilot Bots requires a player-hosted match.

## Paragon pilot kits

Both pilot kit slots share one pool. Choose two different kits, or leave Kit 2 empty.

- Enhanced Parkour adds 13% pilot movement speed and retains the longer wallruns and wallhangs.
- Quick Aim reduces the time to aim down sights by 20%.
- Minion Detector displays friendly and enemy Grunts and Spectres on your minimap while equipped.

Existing preview installs can run the same installer to update. If you use Katie's Reticle Mod, apply the updated optional compatibility ZIP too.

## Credits

PMB by dmitryalexander. Thanks to the [R1Delta contributors](https://github.com/r1delta/r1delta), [Wulfheart and Pilot Bots contributors](https://github.com/lcvb1997/R1Delta-PilotBots-Mod), and [Katie](https://github.com/KatDiedAgain/Kat-R1D-Mods). Titanfall and its game assets belong to their respective owners.
