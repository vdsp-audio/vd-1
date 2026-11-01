# VD-1

A lo-fi drum machine plugin built around a simulated DSP chip: swap the chips, load different
firmware. CLAP and VST3 for macOS, Windows and Linux, plus AU on macOS.

**Website:** https://vdsp-audio.com

This repository holds the releases and the issue tracker. The source code is not public.

## Download

| Platform | File |
|---|---|
| macOS 12 or later (CLAP, VST3, AU; Apple silicon and Intel) | [`VD-1-macOS.zip`](https://github.com/vdsp-audio/vd-1/releases/latest/download/VD-1-macOS.zip) |
| Windows 10 or 11, x64 (CLAP, VST3) | [`VD-1-Windows.zip`](https://github.com/vdsp-audio/vd-1/releases/latest/download/VD-1-Windows.zip) |
| Linux x86_64 (CLAP, VST3) | [`VD-1-Linux-x86_64.tar.gz`](https://github.com/vdsp-audio/vd-1/releases/latest/download/VD-1-Linux-x86_64.tar.gz) |

Install: unpack the download, move the formats your host uses into their folders, then rescan
plugins in your host. [INSTALL.txt](INSTALL.txt) has the same steps as plain text.

### macOS

| Format | Bundle | Folder |
|---|---|---|
| CLAP | `VD-1.clap` | `~/Library/Audio/Plug-Ins/CLAP/` |
| VST3 | `VD-1.vst3` | `~/Library/Audio/Plug-Ins/VST3/` |
| AU | `VD-1.component` | `~/Library/Audio/Plug-Ins/Components/` |

The plugins are signed and notarized by Apple, so macOS opens them without a warning.

### Windows

| Format | File | Folder (administrator) | Or, per user |
|---|---|---|---|
| CLAP | `VD-1.clap` | `C:\Program Files\Common Files\CLAP\` | `%LOCALAPPDATA%\Programs\Common\CLAP\` |
| VST3 | `VD-1.vst3` | `C:\Program Files\Common Files\VST3\` | `%LOCALAPPDATA%\Programs\Common\VST3\` |

The plugin is not signed. The panel needs the Microsoft Edge WebView2 Runtime, which Windows 11 and current
Windows 10 already have. Tested in Bitwig Studio and REAPER.

### Linux

| Format | Files | Folder |
|---|---|---|
| CLAP | `VD-1.clap` and its panel helper `VD-1-editor`, side by side | `~/.clap/` |
| VST3 | `VD-1.vst3` | `~/.vst3/` |

The panel needs WebKitGTK 4.1:

| Distribution | Package |
|---|---|
| Arch | `webkit2gtk-4.1` |
| Debian, Ubuntu | `libwebkit2gtk-4.1-0` |
| Fedora | `webkit2gtk4.1` |

Without it VD-1 still plays, and the host shows its generic parameter sliders instead of the panel.
Tested in Bitwig Studio and REAPER.

### Formats

The formats are the same instrument and share projects and the drive. The VST3 and AU are
made from the CLAP with [clap-wrapper](https://github.com/free-audio/clap-wrapper), and a few things
depend on the format: Bitwig's remote controls are CLAP only, MIDI out works in CLAP and AU but not
VST3, and MIDI clock in is CLAP only (VST3 and AU follow the host's transport).

## Feedback

- **Bugs:** [open an issue](https://github.com/vdsp-audio/vd-1/issues/new?template=bug_report.yml)
- **Ideas:** [open an issue](https://github.com/vdsp-audio/vd-1/issues/new?template=feature_request.yml)
- **Security:** see [SECURITY.md](SECURITY.md); please don't file a public issue.

## License

VD-1 is freeware: free to use, including commercially, and what you make with it is yours. It is
not open source, and it may not be redistributed. See [LICENSE.md](LICENSE.md) and
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

---

VD-1 by vdsp-audio. Not affiliated with Elektron.
