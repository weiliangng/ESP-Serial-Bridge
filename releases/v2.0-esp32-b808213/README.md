# ESP-Serial-Bridge v2.0-esp32-b808213

Immutable ESP32 DevKit firmware snapshot from source commit
`b808213ef88063a63280170b72387edf6b119964`.

## Flash in ESPWebTool

1. Open <https://esptool.spacehuhn.com/> in Chrome or Edge and connect the
   ESP32 Dev Module.
2. Add `ESP-Serial-Bridge-v2.0-esp32-b808213.bin`.
3. Set its address to `0x0` and select **Program**.

This is a single raw image containing the original build outputs at their
required offsets: bootloader at `0x1000`, partitions at `0x8000`, OTA boot data
at `0xe000`, and application at `0x10000`. It targets a 4 MB ESP32 Dev Module.
Do not add the component files a second time.

The image intentionally uses the current `config.h` Wi-Fi/AP settings
unchanged. It is designed for one active bridge in a local setup: every
flashed unit advertises the same AP identity and static address
(`192.168.4.1`), so do not operate multiple units simultaneously in the same
area. Treat these settings and this firmware as public.

| Setting | Value |
| --- | --- |
| SSID | `3301` |
| Password | `33013401` |

## Integrity

| File | SHA-256 | Size |
| --- | --- | ---: |
| `ESP-Serial-Bridge-v2.0-esp32-b808213.bin` | `51545EED2648FE27DB39D22E2CF32A77D55CD4C093EF7022E1A48375CF8FE3E6` | 863,696 bytes |
