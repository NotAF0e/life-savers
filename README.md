# life-savers
## Fix nvidia random stutters
Create `/etc/modprobe.d/nvidia.conf`. Inside write `options nvidia NVreg_RegistryDwords="PerfLevelSrc=0x2222"`

This sets the power mode to max perf at all times which completely removes the variable stutter.

## Force speakers to never turn off automatically to fix speaker pop
Create `/etc/modprobe.d/audio-powersave.conf`. Inside write:
```
options snd_hda_intel power_save=0
options snd_hda_intel power_save_controller=N
```

Rebuild your initramfs using whatever command is relevant to your distro. E.g. `sudo dracut -f` for fedora
