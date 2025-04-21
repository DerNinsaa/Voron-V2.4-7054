# Voron V2.4 7054 Configuration

This repository contains all configuration files for my custom-built Voron V2.4 7054 3D printer.  
It serves as a centralized location for version control, sharing, and backup of my printer's setup.

## Repository Purpose

- **Version Control**: Track changes to configuration files over time.
- **Backup**: Safeguard against data loss due to hardware failures or accidental deletions.
- **Sharing**: Provide insights and configurations to the Voron community.

## Printer Overview

- **Model**: Voron V2.4 7054
- **Firmware**: [Kalico](https://github.com/KalicoCrew/kalico)
- **Control Interface**: [Fluidd](https://github.com/fluidd-core/fluidd) & [KlipperScreen - HappyHare Edition](https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition), [HappyHare](https://github.com/moggieuk/Happy-Hare)
- **Microcontroller**: BTT Manta M8P v2 with CM4, BTT SB2209 Toolhead, BTT MMB ERCF

## Installed Mods

- **G2E** - Extruder 
- **Titanium Extrusion Backers**
- **TheFilter Double + One Single**
- **Kit Printer** - From Lecktor (Pro Version)
- **ERCF v2** - Multimaterial Unit [GitHub](https://github.com/Enraged-Rabbit-Community/ERCF_v2), 8 Channel Version, based on [Siboor Kit](https://docs.siboor.com/siboor-ercf-v2)
- **Blobifier** - [GitHub](https://github.com/Dendrowen/Blobifier)
- **G2E Filametrix** - G2E Version with Leverswitches, based on [GitHub](https://github.com/juliusjj25/G2E-Filametrix-Lever-Switch-Mod)
- Many More little Mods and Things!

## Configuration Files
The Configuration Files are separated according to purpose or connected MCU:

- `printer.cfg`: Main configuration file, has the others included, as well as basic settings for klipper/kalico
- `macros.cfg`: My modified Macros
- `mainboard.cfg`: Manta M8P Configuration
- `toolhead.cfg`: BTT EBB2209 Configuration
- `toolhead_cartographer.cfg`: Cartographer Settings
- `toolhead_leds.cfg`: LED control settings for the toolhead.
- `stepper-tune.cfg`: Stepper motor tuning parameters.
- `mmu/`: Folder containing additional MMU-related configurations.

## Backup and Versioning Strategy

To maintain a reliable backup and version history of the printer's configuration:

1. **Git Integration** – The `printer_data/config` directory is initialized as a Git repository.
2. **Automated Commits** – A script (`autocommit.sh`) automatically commits changes.
3. **GitHub Remote** – Changes are pushed to this GitHub repository for remote backup.
4. **Macro Integration** – A Klipper macro (`BACKUP_CFG`) allows triggering backups from the printer interface.

> For detailed setup instructions, refer to the [Voron Documentation on Backing up Printer Configuration Files to GitHub](https://docs.vorondesign.com/community/howto/EricZimmerman/BackupConfigToGithub.html).

## Usage

To utilize this configuration:

```bash
git clone https://github.com/DerNinsaa/Voron-V2.4-7054.git
