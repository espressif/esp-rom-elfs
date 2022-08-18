# ESP32 series ROM ELF files

The [Releases](https://github.com/espressif/esp-rom-elfs/releases) page of this repository is used to publish the ELF files of ROMs used by ESP32 series of chips.

The releases will be updated whenever a new Espressif chip or a chip revision is released.

## Choosing the ROM ELF file

Files in the release archives have the following naming pattern:
```
<CHIP_NAME>_rev<REV>_rom.elf
```

- `<CHIP_NAME>` — the name of the chip, lower case, without hyphens. For example, `esp32`, `esp32c3`, `esp32s2`.

- `<REV>` — chip revision. You can check the revision of a chip either using `esptool.py chip_id` command or using ESP-IDF API `esp_chip_info`. If the archive doesn't contain the ROM ELF file for your chip revision, use the next lower one.

  For example, for ESP32 rev. 0 and rev. 1, use `esp32_rev0_rom.elf`.

## Copyrights and License

The ROMs of ESP32 series of chips are Copyright (c) 2015-2022 Espressif Systems (Shanghai) Co. Ltd.

The ROMs also include various third-party libraries. The list along with the respective licenses is available [here](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/COPYRIGHT.html#rom-source-code-copyrights).

The ROM code of the currently available ESP32 series of chips is not open-source.

You can use the ELF files in this repository under the terms of Apache License 2.0, provided in the file [LICENSE](LICENSE).

Despite the fact that Apache license is usually applied to software in the source form, the license is also applicable to the compiled files. In the license text this case is referred to as _"Object" form_. We chose to release the ROM ELF files under this license because that makes it easier to use these ELF files in the context of other Apache licensed projects.
