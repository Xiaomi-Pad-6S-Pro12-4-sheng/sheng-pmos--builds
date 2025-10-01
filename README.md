# Warning
We're not responsible for bricked devices, missing recovery partitions, dead xiaomi factoryline workers cowboys, dead microSD cards, dead pmics, dead ram, dead display ics, dead cpus, any xiaomi shenanigans, dead cats or dogs, nuclear wars or you getting fired because you forgot to boot back in to android for the alarm.

All the files here have been contributed by other users, here you will find a guide with the working files we managed to get. This is a delicate process, do it under your own risk and follow all the steps carefully.

**IF YOU AREN'T COMFORTABLE MODDING YOUR TABLET OR ITS PARTITION TABLE OR YOU ARE PARANOID OF BRICKING YOUR DEVICE CLICK AWAY NOW!!! YOU HAVE BEEN WARNED, YOU ARE ON YOUR OWN IF YOU BRICK YOUR DEVICE!!! AGAIN! YOU HAVE BEEN WARNED!!!**


# Installation Guide
Please follow the guide carefully

1. Make sure you have unlocked the bootloader on your device and make sure only Android OS is installed.
2. Look for the latest workflow run (marked with 🟢)
3. Download the desired image:
 - xiaomi-sheng-none_*.zip (minimal system)
 - xiaomi-sheng-plasma_*.zip (KDE Plasma)
 - xiaomi-sheng-gnome_*.zip (GNOME Shell)
 - xiaomi-sheng-gnome_mobile_*.zip (GNOME Shell Mobile)
 - xiaomi-sheng-plasma_mobile_*.zip (KDE Plasma Mobile)
 - xiaomi-sheng-lomiri_*.zip (KDE Plasma Mobile)
 - xiaomi-sheng-kernel_*.zip (kernel packages)
4. Extract ZIP


# Single Boot
1. Boot to bootloader
    ```bash
	adb reboot bootloader
	```
2. Erase dtbo
    ```bash
	fastboot erase dtbo_a
    fastboot erase dtbo_b
	```

3. Flash boot image
    ```bash
	fastboot flash boot_ab boot-xiaomi-sheng.img
	```

4. Flash rootfs image
    ```bash
	fastboot flash userdata rootfs-xiaomi-sheng-*.img
	```

5. Reboot
    ```bash
	fastboot reboot
	```

# Dual Boot
Soon