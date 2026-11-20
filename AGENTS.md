# ADS1262_Fixed

Arduino library for the ADS1262 32-bit ADC. A modified copy of ProtoCentral's `ProtoCentral_ads1262` (not a GitHub fork): the owner removed an unused variable that caused a compiler warning (see `CHANGELOG.md`). Dormant.

- Code: `src/ads1262.cpp` and `src/ads1262.h`. Metadata: `library.properties` and `library.json`.
- Pin assignments are fixed constants in `src/ads1262.h`. The README says to edit that header to change them.
- The repository documents no build command and has no tests. `README.md` mentions `/examples` and `/extras`, but neither folder exists here.
- `arduSeis` pulls this repository by `platformio.ini` at `#main`, so a change on `main` changes that firmware.
- Keep the MIT licence and the ProtoCentral attribution.
