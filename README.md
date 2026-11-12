<div align="center">

<img src="snap/gui/siyuan.png" alt="SiYuan logo" width="128" />

# SiYuan

**A privacy-first personal knowledge base built on blocks**

[![siyuan](https://snapcraft.io/siyuan/badge.svg)](https://snapcraft.io/siyuan)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [SiYuan](https://github.com/siyuan-note/siyuan), a personal knowledge management system with block-level references, WYSIWYG Markdown editing and notes stored on your own computer.

</div>

---

## Getting Started

<a href="https://snapcraft.io/siyuan"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install siyuan
siyuan
```

The command-line interface is `siyuan.cli`, for example `siyuan.cli notebook list -w ~/SiYuan`.

## Configure

There are no `snap set` options; SiYuan is configured in its own settings.

| Data | Location |
| --- | --- |
| Default workspace | `~/snap/siyuan/common/SiYuan` |
| Workspace list, window state and logs | `~/snap/siyuan/common/.config/siyuan` |
| Browser profile and cache | `~/snap/siyuan/common/.config/SiYuan-Electron` |

Optional connections:

```bash
sudo snap connect siyuan:audio-record       # record audio into a note
sudo snap connect siyuan:removable-media    # workspaces and exports on /media or /mnt
```

## Limitations

- Workspaces, imports and exports must be in your home directory, or on removable media once connected. Hidden home folders are out of reach.
- A native installation's settings in `~/.config/siyuan` are not read; its workspace can be selected.
- Local MCP servers cannot start programs installed on your system, such as `npx` or `uvx`.
- Updates come from snapd; the in-app update check is disabled.

## Build

```bash
git clone https://github.com/sidalit/siyuan-snap.git
cd siyuan-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/siyuan-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/siyuan-note/siyuan/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/siyuan-snap/blob/main/LICENSE).
