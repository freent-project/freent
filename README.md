# FreeNT

The OpenWindows vanilla kernel.

## Install

### OpenWindows

OpenWindows already comes with a FreeNT kernel. However, OpenWindows installs a Win32 support layer,
so you can remove it by installing a vanilla version of FreeNT:

1. Enable [developer mode](https://freent-project.github.io/openwindows11-docs/dev-mode).
2. Press Ctrl+Alt+Shift+OpenWindows+F5 to open a console as the SYSTEM user.
3. Run `usekernel https://freent-project.github.io/kernel-bin-latest` to grab a kernel from FreeNT.
   **This will overwrite all your data, effectively factory resetting your settings
    and wiping the system partition! Your device will be stuck in developer mode until you run
   `usekernel openwindows`!**
5. You will get a menu to select either "OpenWindows 11" or "FreeNT 3.1". The difference is that
   "OpenWindows 11" boots OpenWindows with the kernel with OpenWindows patches (most of which are
   done via modules), while "FreeNT 3.1" boots OpenWindows with the plain kernel.
6. If you want to remove the menu, get the [`nuke-owboot-menu` module](https://github.com/freent-project/freent-module-nuke-owboot-menu).

### Other systems

**This will mess up Unix-style partitions, and break Linux apps! This can render Linux systems
useless!**

1. [Download](https://freent-project.github.io/kernel-iso-latest) the kernel and connect an external disk,
   e.g. a USB.
3. Write the downloaded ISO `freent-3.1-vanilla.iso` to the disk.
4. Boot from the disk. Your old OS will be detected and will be reinstalled with its official kernel
   and bootloader removed, and replaced with FreeNT and OWBoot respectively.
