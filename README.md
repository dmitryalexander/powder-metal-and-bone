# Powder, Metal & Bone

PMB is a Titanfall 1 mod for R1Delta private matches. Paragon opens with IMC versus Militia in Operator, then switches to free-for-all in Candidate. In the finale, kill the Paragon to take the title. The current holder wins when the shared timer expires. A separate kill clock passes the title if the holder goes too long without a kill.

**Paragon - Live Fire** uses the six Live Fire maps, shorter phases, respawns and a first-to-three round format. To play the imported maps, configure R1Delta to use your local Titanfall 2 installation.

**[Download BETA Preview 1](https://github.com/dmitryalexander/powder-metal-and-bone/releases/download/v0.6.0-beta.preview.1/Powder-Metal-and-Bone-v0.6.0-beta.preview.1.zip)** for the V-47 Flatline, Data Knife melee, and the latest Paragon updates. The ZIP installs both PMB addons. Enable **POWDER METAL & BONE** and **POWDER METAL AND BONE BETA** in R1Delta’s **Addons** menu.

## Requirements and installation order

1. **Newest R1Delta required.** Install [R1Delta 3.0.5 Escrow 6](https://github.com/r1delta/r1delta/releases/tag/v3.0.5), the version this PMB package targets.
2. **Pilot Bots required.** Install [Pilot Bots 2.1.7](https://github.com/lcvb1997/R1Delta-PilotBots-Mod/releases/tag/Pilot-bots-v2.1.7) into the same R1Delta version. Use the original author's installer.
3. **Install PMB.** Download and extract the main ZIP from [BETA Preview 1](https://github.com/dmitryalexander/powder-metal-and-bone/releases/tag/v0.6.0-beta.preview.1). Close Titanfall and the launcher. Run the included installer against the R1Delta application folder and the Titanfall game folder.
4. **Katie's Reticle Mod is optional.** Install [Katie's Reticle Mod at the supported revision](https://github.com/KatDiedAgain/Kat-R1D-Mods/tree/4b3a530cd2f6bca040bbab463f8cf647d4d18041/Katies_Reticle_Mod) and apply the separate PMB compatibility ZIP from the release. Follow the instructions in that ZIP so Katie's sway fix and PMB's weapon settings work together.

**Frontier Overhaul is incompatible.** Disable it before running PMB.

## Install PMB

Open PowerShell in the extracted ZIP folder. Pass the folder that contains `Titanfall.exe` and its `r1delta` subfolder as `RuntimeRoot`. Pass the Titanfall content folder that contains `r1` and `vpk` as `GameRoot`.

```powershell
.\Install-PMB.ps1 -RuntimeRoot 'C:\path\to\R1Delta\app-3.0.5' -GameRoot 'C:\path\to\Titanfall'
```

Add `-CheckOnly` to check the files before installation. The installer checks the required versions and package files, saves replaced files to a backup folder, and reports its location. Restart R1Delta, open **Addons**, and enable both **POWDER METAL & BONE** and **POWDER METAL AND BONE BETA**. Select **Private Match → Paragon**.

Use the same PMB and dependency versions on the host and each player's PC. This is a multiplayer preview. A full match with a remote second player still needs testing. Pilot Bots requires a player-hosted match.

## Pilot loadouts

In PMB multiplayer, choose two different tacticals and two different pilot kits. Both secondary slots can be left empty.

- Enhanced Parkour adds 13% pilot movement speed and retains the longer wallruns and wallhangs.
- Quick Aim reduces the time to aim down sights by 20%.
- Minion Detector and enemy death reports are active automatically.
- Tactikill refills both tacticals on an enemy pilot kill. Blast Padding reduces splash damage by 60%.
- Ghost slows ordinary lock-on acquisition. Scramble jams radar and lock-ons.
- MOLTOV and Electric Smoke are available as pilot ordnance.

Existing preview installs can run the same installer to update. Continuous Radar is now part of PMB. On upgrade, the installer moves the previous standalone PMB.Continuous_Radar folder into a dated backup under the game’s r1 folder. If you use Katie's Reticle Mod, apply the updated optional compatibility ZIP too.

## Credits

PMB by dmitryalexander. Thanks to the [R1Delta contributors](https://github.com/r1delta/r1delta), [Wulfheart and Pilot Bots contributors](https://github.com/lcvb1997/R1Delta-PilotBots-Mod), and [Katie](https://github.com/KatDiedAgain/Kat-R1D-Mods). Titanfall and its game assets belong to their respective owners.

The lobby uses the stock Titanfall movie from `r1/media/menu_act01.bik`. The installer links it under PMB’s lobby filename, with a local copy on filesystems that lack hard links. The lobby movie is sourced from your Titanfall installation.

The installer expands the packaged Ogg Vorbis music into the PCM WAV files used in game.
