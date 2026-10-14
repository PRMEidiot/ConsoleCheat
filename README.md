# ConsoleCheat# cs16-py

External CS 1.6 cheat. Python 3.10+, Windows 10/11.

## install
    pip install -r requirements.txt

## run
    python cs16.py

Game must be running first. Run terminal as admin.

## hotkeys
- F1 - toggle aimbot
- F2 - toggle ESP
- hold LMB - aim when aimbot is on

## offsets
offsets.py holds client.dll offsets for build 4554. If RPM returns
garbage, re-derive with Cheat Engine:
- DW_LOCAL_PLAYER - pointer that dereferences to your player struct
- DW_ENTITY_LIST  - base of the array of entity pointers
- DW_VIEW_MATRIX  - 16 floats, the current view projection

## detection
VAC 1.6 scans client.dll .text only. This cheat is external - RPM/WPM
from another process. No injection, no game-module writes except view
angles. Non-Steam builds have no anticheat.
