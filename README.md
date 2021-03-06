# klipper_config

Base working config for a Voron 2.4 r1.5 (yes, between a 1 and a 2) 350mm printer

Autocommit created using:
- Kiauh - for the G-code shell script
- Andrew Ellis - Voron guide for the gitbackup.cfg file
- Lazaro Film guide on creating the github for the first time - https://lazarofilm.gitbook.io/3d-printing/creating-a-github-backup-for-klipper

# Change log
### 20220423
- changed the `sample_retract_dist:` setting in the `[probe]` section to match Andrew Ellis at 0.35 as well as the `homing_retract_dist:` in the `[stepper_z]` section.
- this makes all the moves that touch the endstop and the klicky probe much faster, but all sorts of issues ensued, probably related to switch bounce and misreading, but caused errors in automatic z-calibration and got lovely holes in the build plate... now set to `sample_retract_dist: 0.75` and `homing_retract_dist: 0.75`. Still faster than the default, but no more issues [ed. took a long time to work that one out]

### 20220421
- changed to spherical bearings on the z-axis and had to update all the endstop positions

### 20220409
- changed Z retract distance in klicky-z-calibration.cfg to make sure the klicky probes clears the z endstop
