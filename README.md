# D868UV-Enhanced

Unofficial K4RJM firmware and Windows CPS for the AnyTone AT-D868UV.

**Firmware compatibility warning.** A stock AT-D868UV must have **hardware version 1.1 (shown as 1.10)** and be **running factory firmware 2.40** before conversion. Before flashing, visually verify both part numbers printed on the chips inside your own radio:

- **GigaDevice GD32F303VGT6** — main processor
- **Toshiba TC58CVG0S3HRAIG** — external NAND flash

The hardware version shown on the screen alone cannot identify those chips. If either prerequisite is unmet or either chip marking cannot be matched, **do not flash this firmware**. An incompatible image can leave the radio unable to boot.

**[Download the 2.43 Windows CPS installer and radio firmware (ZIP)](https://github.com/K4RJM/D868UV-Enhanced/releases/download/v2.43/D868UV-Enhanced-2.43.zip)**

1. In Windows, right-click `D868UV-Enhanced-2.43.zip` and choose **Extract All**.
2. Run `Setup-2.43.exe` and open **D868UV Enhanced CPS 2.43** from the Start menu. The CPS uses the stock D868UVE Windows runtime. On a new PC, install the manufacturer's D868UVE CPS 1.40 first.
3. Back up your codeplug and keep your recovery firmware. To update the radio, open the extracted **Firmware** folder and select `D868UV_2.43.SPI` in the D868 firmware updater. Keep the matching CDI and CDD beside it.
4. Use **Optional Setting > Display** in the CPS to adjust colors, indicators and date/time formats. Save and write the codeplug to apply those settings.

The 2.43 standby display was tested on an AT-D868UV with hardware 1.10 and a GD32F303VGT6. If you already run 2.43 Test 2, the release has the same radio firmware and you can install the matching CPS directly.

[2.43 release notes](https://github.com/K4RJM/D868UV-Enhanced/releases/tag/v2.43) · [Previous release (2.41)](https://github.com/K4RJM/D868UV-Enhanced/releases/tag/v2.41)
