---
weight: 300
date: "2023-06-08T19:25:22+01:00"
draft: false
title: "Quickstart"
icon: "rocket_launch"
# featured_image: ""
description: "A guide to getting up and running with a altOS."
---

## Requirements

- A Chromebook
- A USB drive larger than 8 gigabytes
- Internet connection
- Yo brain

## Step 1: Enabling Developer Mode

1. Press the `esc` + `refresh` + `power` buttons all at once on your Chromebook. Doing so will bring you to a screen that will prompt you to insert a USB stick or SD card.
2. On that screen, press `ctrl` + `d`. It will prompt you if you want to turn off OS verification. Press `ENTER`. Your Chromebook will restart and present a screen that says OS verification is OFF.
3. ChromeOS will then display a message for 30 seconds about transitioning the system to developer mode.
4. Once done, the Chromebook will restart into developer mode. Now, you can flash custom firmware.


## Step 2: Disabling Write Protection:
Check the type of WP you have on the supported devices page. Depending on your device, your steps will vary slightly:

**Screw**
Open up the back of your Chromebook, and look for a write protect screw. Unscrew it and throw it away.

**Battery**
Open the back of your Chromebook, unplug the battery, then plug in the charger and flash firmware.

**Jumper**
uhhh


## Step 3: Firmware

To keep it breif, UEFI firmware allows the Chromebook to become any other laptop. This means you will lose access to chromeOS. RW_Legacy allows you to dualboot chromeOS along with Linux.

1. Open a terminal via VT-2 by pressing `ctrl` + `alt` + `→`.
2. Log in as user `chronos`. Note that there should be no password unless you set one yourself.
3. Run the Firmware Utility Script:
  ```shell
cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
```

If you encounter certificate related errors when downloading the script from ChromeOS, then add -k to the curl command and script command to bypass SSL certificate checking as so:
```shell
cd; curl -LOk mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
```

{{< alert context="warning" text="The Firmware Utility Script cannot be run from a crosh shell, or a crostini shell." />}}

4. Select the firmware you would like to flash.
5. Follow the on-screen prompts. Once you are done, you should reboot into the new firmware! Keep in mind that the first boot will always take longer due to a process called "memory training". DO NOT power off the device at any time during the first boot.

## Step 4: altOS
todo
