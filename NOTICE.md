# Third-party notices

The AirLock firmware binaries distributed in this repository are derived
works that statically link the open-source libraries listed below. Each
library remains under its own license; the inclusion of these binaries
in this repository does not change those terms.

## Libraries linked into the firmware

| Library | License | Upstream source |
|---|---|---|
| arduino-esp32 (ESP32 Arduino core, incl. ESP-IDF transitively) | Apache-2.0, with LGPL-2.1 components and various permissive sub-licenses | <https://github.com/espressif/arduino-esp32> |
| Adafruit GFX Library | BSD-3-Clause | <https://github.com/adafruit/Adafruit-GFX-Library> |
| Adafruit SSD1306 | BSD-3-Clause | <https://github.com/adafruit/Adafruit_SSD1306> |
| Adafruit NeoPixel | LGPL-3.0 | <https://github.com/adafruit/Adafruit_NeoPixel> |
| Encoder (Paul Stoffregen) | MIT / public domain | <https://github.com/PaulStoffregen/Encoder> |
| ESP32Servo | LGPL-3.0 | <https://github.com/madhephaestus/ESP32Servo> |
| CodeCell | Apache-2.0 | <https://github.com/microbots-io/CodeCell> |

## LGPL components — your relinking right

Two of the libraries above (Adafruit NeoPixel, ESP32Servo) plus parts of
arduino-esp32 are licensed under the **GNU Lesser General Public License
(LGPL)**. Because the AirLock firmware statically links these libraries,
the LGPL grants you, as the recipient of the binaries, the right to
modify the LGPL-licensed code and relink it into a working firmware
image — even though the AirLock-specific code is proprietary.

To exercise that right, the LGPL requires us to make available either
the source of the LGPL components or the unlinked object files of the
non-LGPL portion of the firmware (so that you can relink them against
your modified LGPL library).

We satisfy this in two ways:

1. **Upstream sources for the LGPL libraries** are at the URLs in the
   table above. The versions used at build time are pinned in the
   AirLock build configuration; if you need the exact commit hashes
   for a specific firmware release, contact us at the address below
   and we'll provide them.
2. **Unlinked object files of the proprietary AirLock components**, in
   a form suitable for relinking with a modified LGPL library, are
   available on request from <licensing@kinkforge.com> for any
   released firmware version, free of charge for the duration of
   LGPL §6's reasonable-time obligation.

If you intend to redistribute a modified firmware, note that the LGPL
also requires you to include this notice and to make the modified
sources of the LGPL components available under the same license.

## AirLock proprietary code

The AirLock-specific code (everything in the firmware that is not part
of the libraries above) is © KinkForge. No license is granted to
redistribute, decompile, sell, or modify the proprietary portion of
the firmware. The "AirLock" name is used as a product identifier;
this notice does not grant trademark rights.

## Disclaimer

This firmware is provided "as is", without warranty of any kind. See
the upstream licenses for the full warranty disclaimers of each
component.
