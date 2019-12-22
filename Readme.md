# Matebook_D_Hackintosh_OpenCore

## Huawei Matebook D 2018(I7 8550U)

| Specifications | Details                                                                                                            |
|:--------------:|:------------------------------------------------------------------------------------------------------------------:|
| Graphics Cards | Intel UHD620 / nVidia MX150                                                                                        |
| Memory         | 8GB*2 DDR4 2400                                                                                                    |
| Keyboard       | PS2 Keyboard with no backlight🙃                                                                                   |
| Trackpad       | ELAN2202(Requires _OSI Patch to enable APCI interrupt)                                                             |
| Sound Card     | ALC256                                                                                                             |
| Screen         | 15.6‘ 1920x1080                                                                                                    |
| SSD            | Hikivision C2000 512GB + LITE-ON 128GB SATA m.2                                                                    |
| WiFi+BT        | Apple Broadcom BCM94360CS2                                                                                         |
| Processor      | Intel Core I5 8250U / I7 8550U (you need to generate a new CpuFridendDataProvider if you have an I5-8250U version) |

---------

## Current Status

* Based on OpenCore Official Release 0.5.3

* Native(?) NVRAM works.

* Soundcard with injected Layout-ID 21 works well.

* CFG Lock cannot be unlocked in Huawei's fxxking BIOS. However everything just works. I'm not able to modify the confusing InsydeH2O BIOS now.

* Replaced stock Intel Wireless 8265AC with BCM94360CS2 with an adapter. Using [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup) with `brcmfx-country=#a`to enable all WiFi channels.

* Use [one-key-cpufriend](https://github.com/stevezhengshiqi/one-key-cpufriend) to gain a better CPU power management.

* DGPU nVidia MX150 is disabled by SSDT-DDGPU.

* Minor bug: Screen backlight requires a second-open to turn on after closing lid.

* This EFI may also works on Magicbook 14 Kabylake. ( Just I guess, it may need some minor modifications)

* You may need to use your own System-UUID when you need dual boot with Windows 10.

------

## TODOs

* Chinese version of this document(简体中文文档会有的，不过现在用翻译器也能看，I'm just lazy)

* Improvements on Hibernation.

* Windows 10 startup item in OpenCore (I think using boot menu is a better choice)

------

## Credits &  Guides

1. [Acidanthera](https://github.com/acidanthera) for OpenCore (and related documents) , Lilu, AppleALC and other awesome projects.

2. [OC-little](https://github.com/daliansky/OC-little) for their handy ACPI Hotpatches for OpenCore.

3. [Justin](https://github.com/cattyhouse) for  [oc-guide](https://github.com/cattyhouse/oc-guide) 

4. [xjn](https://github.com/xjn819) for [《使用OpenCore引导黑苹果》](https://blog.xjn819.com/?p=543)

5. Daliansky, bat.bat

6. [Steve Zheng](https://github.com/stevezhengshiqi) for [one-key-cpufriend](https://github.com/stevezhengshiqi/one-key-cpufriend) and [XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)

7. The Clover EFI I have used by [MOJUNSHOU](https://github.com/MOJUNSHOU) : [MateBooK-D](https://github.com/MOJUNSHOU/MateBooK-D)

-----


