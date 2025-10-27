# yuna0x0's Arch User Repository (AUR) Packages
This repository contains package sources for AUR packages maintained by [yuna0x0](https://aur.archlinux.org/packages?K=yuna0x0&SeB=m) using [aurpublish](https://github.com/eli-schwartz/aurpublish).

## Setup
Steps to set up environment for maintaining AUR packages with `aurpublish`:

1. **Install `aurpublish`**:
```bash
sudo pacman -S aurpublish
```

2. **Clone this repository**:
```bash
git clone https://github.com/yuna0x0/aur.git yuna0x0-aur
cd yuna0x0-aur
```

3. **Setup git hooks**:
```bash
aurpublish setup
```

## License
Visit each package's directory for specific license information.

Package sources that are created by yuna0x0 follow Arch Linux [RFC 40](https://rfc.archlinux.page/0040-license-package-sources/), which are licensed under [0BSD](https://spdx.org/licenses/0BSD.html).

Package sources that are modified from other maintainers might not have a license, due to Arch Linux not having a license for package sources before RFC 40. If there's any question regarding those package sources, please open an issue in this repository.
