# life-savers
## Fix nvidia random stutters
Create `/etc/modprobe.d/nvidia.conf`. Inside write `options nvidia NVreg_RegistryDwords="PerfLevelSrc=0x2222"`

This sets the power mode to max perf at all times which completely removes the variable stutter.

