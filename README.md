# xanmod-kernel-WSL2
![Kernel CI](https://github.com/Zugfritze/xanmod-kernel-WSL2/actions/workflows/build.yml/badge.svg?branch=main)
![](https://img.shields.io/github/license/Zugfritze/xanmod-kernel-WSL2)
![version](https://badgen.net/github/release/Zugfritze/xanmod-kernel-WSL2)

Unoffical [XanMod](https://github.com/xanmod/linux) port with [dxgkrnl](https://github.com/microsoft/WSL2-Linux-Kernel/tree/linux-msft-wsl-5.15.62.1/drivers/hv/dxgkrnl) patched for **WSL2**, compiled by [clang](https://clang.llvm.org/) with ThinLTO enabled.

This repo holds an automated **GitHub Action** workflow to build and release WSL kernel images. It checks if newer upstream version is available everyday, and trigger the build&release process accordingly. 

## Usage

### Manual Installation

* Download kernel image from [releases](https://github.com/Zugfritze/xanmod-kernel-WSL2/releases).
* Place it to somewhere appropriate. (e.g. `D:\.WSL\bzImage`) 
* Save the `.wslconfig` in current user's home directory with following content:
```ini
[wsl2]
kernel = the\\path\\to\\bzImage
; e.g.
; kernel = D:\\.WSL\\bzImage
;
; Note that all `\` should be escaped with `\\`.
```
* Reboot your WSL2 to check your new kernel and enjoy!

> For more information about `.wslconfig`, see microsoft's official [documentation](https://docs.microsoft.com/en-us/windows/wsl/wsl-config#configure-global-options-with-wslconfig).

## Credits

* The Linux community for the awesome OS kernel.
* Microsoft for WSL2 and dxgkrnl patches.
* XanMod project for various optimizations.
