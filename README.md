# klipper_config

Base working config for a Voron 2.4 r1.5 (yes, between a 1 and a 2) 350mm printer

Autocommit created using:
- Kiauh - for the G-code shell script
- Andrew Ellis - Voron guide for the gitbackup.cfg file
- Lazaro Film guide on creating the github for the first time - https://lazarofilm.gitbook.io/3d-printing/creating-a-github-backup-for-klipper

# Change log
### 20230617
- Updated the entire codebase from Mainsail OS from dusty to bullseye
- Crowsnest is now used for the Webcams - so two less config files

### 20230125
- changed from LGX Lite to Orbiter 2.0 extruder - much better feed, esp with PA6-CF, my most challenging filament to get right

### 20230115
- changed from CW2 extruder to LGX Lite - didn't go so well, only two settings for pressure, poor feed on uneven filaments

### 20230105
- changed to Voron Tap instead of klicky probe - much better reliability of probing

### 20220922
- changed to an umbilicus using the BTT EBB board with all the config changes to go with it

### 20220903
- implemented active chamber heating code using a DBK PTC heater and a SSR
- will also actively exhaust the chamber is it is overheating from the bed
- changed lcd-tweaks.cfg to show chamber temp and targets

### 20220423
- changed the `sample_retract_dist:` setting in the `[probe]` section to match Andrew Ellis at 0.35 as well as the `homing_retract_dist:` in the `[stepper_z]` section.
- this makes all the moves that touch the endstop and the klicky probe much faster, but all sorts of issues ensued, probably related to switch bounce and misreading, but caused errors in automatic z-calibration and got lovely holes in the build plate... now set to `sample_retract_dist: 0.75` and `homing_retract_dist: 0.75`. Still faster than the default, but no more issues [ed. took a long time to work that one out]

### 20220421
- changed to spherical bearings on the z-axis and had to update all the endstop positions

### 20220409
- changed Z retract distance in klicky-z-calibration.cfg to make sure the klicky probes clears the z endstop
