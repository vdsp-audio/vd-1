# VD-1

A lo-fi drum machine plugin built around a simulated DSP chip: swap the chips, load different
firmware. CLAP, VST3 and AU for macOS; Windows and Linux next.

**Website:** https://vdsp-audio.com

This repository holds the releases and the issue tracker. The source code is not public.

## Download

| Platform | File |
|---|---|
| macOS 12 or later (CLAP, VST3, AU; Apple silicon and Intel) | [`VD-1-macOS.zip`](https://github.com/vdsp-audio/vd-1/releases/latest/download/VD-1-macOS.zip) |

Install: unzip, then move the format your host uses into its folder and rescan plugins in your
host:

| Format | Bundle | Folder |
|---|---|---|
| CLAP | `VD-1.clap` | `~/Library/Audio/Plug-Ins/CLAP/` |
| VST3 | `VD-1.vst3` | `~/Library/Audio/Plug-Ins/VST3/` |
| AU | `VD-1.component` | `~/Library/Audio/Plug-Ins/Components/` |

The plugins are signed and notarized by Apple, so macOS opens them without a warning.

The three formats are the same instrument and share projects and the drive. The VST3 and AU are
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
