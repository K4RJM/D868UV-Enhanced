# D868UV-Enhanced

Unofficial K4RJM firmware and Windows CPS for the AnyTone AT-D868UV.

**Firmware compatibility warning.** A stock AT-D868UV must have **hardware version 1.1 (shown as 1.10)** and be **running factory firmware 2.40** before conversion. Before flashing, visually verify both part numbers printed on the chips inside your own radio:

- **GigaDevice GD32F303VGT6** — main processor
- **Toshiba TC58CVG0S3HRAIG** — external NAND flash

The hardware version shown on the screen alone cannot identify those chips. If either prerequisite is unmet or either chip marking cannot be matched, **do not flash this firmware**. An incompatible image can leave the radio unable to boot.

**[Download the 2.43 firmware, AnyTone firmware flasher and Windows CPS installer (ZIP)](https://github.com/K4RJM/D868UV-Enhanced/releases/download/v2.43/D868UV-Enhanced-2.43.zip)**

The firmware, factory flasher and Windows CPS are available for no charge.

## Programmable keys carried forward from 2.41

Eight added shortcuts bring the D868UV from 38 to 46 assignable functions. Choose them under **Optional Setting > Key Function**. The choices depend on the button and whether you select a short or long press.

1. **Zone Select** opens zone selection.
2. **Mute timing** mutes receive audio for 1–256 minutes. Set the duration under **Optional Setting > Other**. Audio returns when the timer expires, or you can press the key again to cancel.
3. **CTC/DCS Set** opens the CTCSS/DCS tone settings.
4. **Gps** switches GPS on or off.
5. **Ch.Name** switches the channel display between name and frequency.
6. **CDT Scan** searches for a matching receive tone or code in the configured CTCSS or DCS family on an analog signal. Press again to restore the channel’s receive filter.
7. **Dim Shut** switches off the display backlight.
8. **ANA SQL** adjusts the analog squelch level.

## Color choices carried forward from 2.41

Under **Optional Setting > Display**, you can set each of these independently.

| CPS setting | What it colors |
| --- | --- |
| Call Sign Display Color | Callsign text |
| A Channel Name Color | Channel A name |
| B Channel Name Color | Channel B name |
| Zone Name Colour A | Channel A’s zone name |
| Zone Name Colour B | Channel B’s zone name |
| Standby Char Color | Standby text |

All six offer **orange, red, yellow, green, turquoise, blue and white**. Standby text also offers **black**.

## Display options added since 2.41

Under **Optional Setting > Display**, you can change these settings in the codeplug and write it to the radio.

- **Display Channel Type** shows or hides the channel-type indicator.
- **Display Time Slot** shows or hides the DMR time slot.
- **Display Color Code** shows or hides the DMR color code. Each of the three indicators has its own switch.
- **Date Display Format** offers `DD-MM-YYYY` (stock), `MM/DD/YYYY`, `DD/MM/YYYY` and `YYYY/MM/DD`.
- **Time Format** offers a 24-hour clock or a 12-hour clock with a capital **A** or **P**. On standby, the date sits on the left and the time on the right.

## Standby screen changes since 2.41

- **Power badges for both channels.** A red badge shows each channel’s transmit-power setting beside its name. Both badges share the same left edge. The larger badge follows the selected channel when you switch between A and B.
- **D890UV-style status icons.** The power indicator moved from the top bar to the channel rows, and the remaining status icons use fixed positions.
- **Battery gauge.** The outline stays white as the battery discharges. The bars are green at full charge.
- **Divider lines.** Removed the line below the status bar and the line above the bottom menu.
- **Bottom menu.** Menu, Zone and List use a 12-pixel font, with the up/down arrows aligned beside Zone.

## Installing the firmware and CPS

1. In Windows, right-click `D868UV-Enhanced-2.43.zip` and choose **Extract All**.
2. Run `Setup-2.43.exe` and open **D868UV Enhanced CPS 2.43** from the Start menu. The CPS uses the stock D868UVE Windows runtime. On a new PC, install the manufacturer's D868UVE CPS 1.40 first.
3. Back up your codeplug and keep your recovery firmware. To install the stock AnyTone firmware flasher, run `Firmware Updater/QXCodePro_Update_dpinst_Setup_1.02.exe` from the extracted ZIP. Open QXCodePro and select `Firmware/D868UV_2.43.SPI`. Keep the CDI and CDD beside it.
4. Use **Optional Setting > Display** in the CPS to adjust colors, indicators and date/time formats. Save and write the codeplug to apply those settings.

The 2.43 standby display was tested on an AT-D868UV with hardware 1.10 and a GD32F303VGT6. If you already run 2.43 Test 2, the release has the same radio firmware and you can install the matching CPS directly.

[2.43 release notes](https://github.com/K4RJM/D868UV-Enhanced/releases/tag/v2.43) · [Previous release (2.41)](https://github.com/K4RJM/D868UV-Enhanced/releases/tag/v2.41)
