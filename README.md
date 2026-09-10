# Dream-disassembly
A disassembly of the unreleased Rareware title named "Dream - Land of Giants"

## Contributing
Contributions to the disassembly are currently primarily focused on the DiztinGUIsh project itself and not directly to the source output.

In order to open the Diz project you'll need to apply the "dream - uncorrupted header title.bps" patch located in the "project" folder using Floating IPS (flips): https://www.smwcentral.net/?p=section&a=details&id=42149. This is required to prevent DiztinGUIsh from throwing an error when trying to verify the title with the internal header since the original ROM dump contains a corrupted title with null bytes in it.

You can download DiztinGUIsh from here: https://github.com/DizTools/DiztinGUIsh/releases/tag/v2.5.1.0

The source output is designed to be built with Asar: https://github.com/RPGHacker/asar/releases/tag/v1.91

## ROM Layout
Dream uses a 16-megabit (2 MB) fast ROM (3.58 MHz) with the HiROM mapping mode. It occupies banks $80–$81 for the program and banks $C0-$DF for data.

### Bank Contents
#### bank $80 ($808000-$80FFFF)
- Main engine code

#### bank $81 ($818000-$81FFFF)
- Sound engine (CPU side)

#### bank $C2 ($C20000-$C2FFFF)
- Sound engine (SPC side)
- BRR sample table
- BRR sample data
- Sample upload data
- Music sequence data
- Sound effect sequence data

#### bank $C4 ($C40000-$C4FFFF)
- Sprite graphics table
- Sprite animation table
- Sprite animations
- Color palette data