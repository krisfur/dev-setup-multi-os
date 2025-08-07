# Windows 11 Setup

## Basic programs to get

In order that makes it least annoying:

- [Firefox](https://www.firefox.com/en-GB/) -> Or other browser you use to keep accounts in sync between devices
- [Nvidia App](https://www.nvidia.com/en-gb/software/nvidia-app/)
- [Rustup](https://www.rust-lang.org/tools/install) -> Also includes `Visual Studio build tools` which will be useful for other compiled languages!
- [Git](https://git-scm.com/downloads/win)
- [GitHub CLI](https://cli.github.com/) -> then run `gh auth login`
- [Visual Studio Code](https://code.visualstudio.com/download) -> After `GitHub CLI` for syncing extensions!
- [Golang](https://go.dev/doc/install)
- [CMake](https://cmake.org/download/)
- [LM Studio](https://lmstudio.ai/)
- [FFMPEG](https://ffmpeg.org/download.html)

Optinal daily life stuff:

- [Discord](https://discord.com/download)
- [Steam](https://store.steampowered.com/about/?dve_trk_id=21e4672c-d466-4260-b532-0221ab94acf7)
- [VLC](https://www.videolan.org/vlc/)
- [Battle.net](https://download.battle.net/en-gb/desktop)
- [GIMP](https://www.gimp.org/downloads/thanks.html)


## Fixing power issues with Asus trackpads

Asus laptops (namely the Proart PX13) suck at power management and by defult the trackpad lags and gets ghost clicks on battery power. Fixing it is a bit involved.

1. Download newest `chipset` and `pointing device` drivers from [Asus support website](https://www.asus.com/uk/laptops/for-creators/proart/proart-px13-hn7306/helpdesk_download?model2Name=HN7306WV).
2. Download `MyAsus`, `ProArt Creator Hub`, and `ASUS Dial & Control Panel` (microsoft store) -> and get all updates!
3. In MyAsus set battery power power management to Windows
4. In Windows Settings -> System -> Power, set battery to `best performance`.
5. In your `cmd` shell run:

```powershell
powercfg /setdcvalueindex SCHEME_CURRENT SUB_PCIEXPRESS ASPM 0
```

and reboot.

### What the Command Does:
- `/setdcvalueindex`: Modifies a specific power setting while the laptop is on Direct Current (i.e., battery power).
- `SCHEME_CURRENT`: Targets the currently active power plan (e.g., "Best Performance").
- `SUB_PCIEXPRESS`: Specifies the PCI Express power settings subgroup.
- `ASPM`: Targets the "Link State Power Management" setting (Active State Power Management).
- `0`: Sets the value to Off (disabling the power-saving feature).

## Screenshot

![windows screenshot](windows.png)