# Wayland on a NVIDIA Graphics Processor
So, you inevitably reinstalled arch, congratulations! Now, you need to fix everything again. Luckily for you, I've been through this often enough that I've decided to write something about it.

## Actually having a usable environment
NVIDIA by default has some _mildly_ insane defaults when it comes to wayland. Thats fair, they got better things to do. But we need them fixed. We need to actually be able to login to a desktop environment.
* ### Loading modules
   You'll want to include some nvidia modules within your bootloader settings, be it dracut or mkinitcpio. [Arch's Wiki](https://wiki.archlinux.org/title/NVIDIA#Early_loading) lists them here.
  This means adding `nvidia`, `nvidia_uvm`, `nvidia_drm`, and `nvidia_modeset` as modules.
  * #### mkinitcpio
    Open `/etc/mkinitcpio.conf` or `/etc/mkinitcpio.conf.d/<custom>.conf` in your favourite text editor as root.
