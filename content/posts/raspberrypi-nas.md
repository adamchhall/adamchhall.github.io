+++ 
draft = true
date = 2026-02-22
title = "Setting up my Raspberry Pi NAS"
outputs = ['html', 'rss']
description = ""
slug = ""
authors = [ "Adam Hall"]
tags = []
categories = []
externalLink = ""
series = []
+++

# A First Step towards Digital Freedom
lorem ipsum dolor

## Installing Raspberry Pi OS (which is basically just Debian)
Any version of the Raspberry Pi Imager less than 2.0.0 seems to fail to write settings appropriately to 
the flashed SD card, resulting in endless headaches when trying to connect to a Pi with a headless configuration
via wifi! Becuase the WiFi password and SSID have not been correctly configured, the device will immidiately and
silently fail to connect to the Internet if this isn't addressed. Your options are to make sure you are using a
very recent version of the Pi Imager, to plug the Pi into a monitor and keyboard to configure it even if you plan
to eventually run it headless, or to find the correct config files to change these settings manually after the
image is flashed.

## Adding More Storage
An SD card isn't enough space for a proper NAS setup, so I'm using a 10 TB HDD attached to the Pi through a
powered USB HDD enclosure. Because this is external media, we need to do a little bit of extra work to get
it set up and auto-mounted to the filesystem.

to find uuid: "sudo blkid"
make directory /mnt/data/
in fstab add "uuid=whatever /mnt/data btrfs defaults,nofail 0 2" at the bottom

create the directory /mnt/data/shared for the NAS root directory. If you anticipate more users being given
access to the NAS later, you can create a home directory for each of them, e.g. /mnt/data/shared/adam,
or /mnt/data/shared/johndoe.

## Sharing with Samba
Once this initial hurdle is out of the way, it is fairly easy to follow the instructions from this
[tutorial](https://www.hackster.io/ElecrowOfficial/diy-nas-network-attached-storage-with-raspberry-pi-5-e91a37)
to get a basic [NAS](https://en.wikipedia.org/wiki/Network-attached_storage) working.

# OK, now what?

lorem ipsum dolor
0
## Install Syncthing
install syncthing
sudo apt install syncthing

needed to change permissions so that my user was the owner of the nas directory

## Backups with Restic

1. Install Restic
sudo apt install restic

2. Create /etc/restic-env with login credentials for backup service. In my case, this was Backblaze B2:
export AWS_ACCESS_KEY_ID=ABC123
export AWS_SECRET_ACCESS_KEY=ABC123
export RESTIC_REPOSITORY="MyRepo"
export RESTIC_PASSWORD_FILE=/etc/restic-password

3. Create /etc/restic-password with your password in it

4. Create the automatic backup script
mybackupscript.sh: 

---
#!/bin/bash
source /etc/restic-env
## Generate backup
restic -r s3:mybackblazeurl backup /mnt/data/
## Handle retention policy
restic -r s3:mybackblazeurl forget --keep-weekly 4 --keep-monthly 12
## Done
---

cron job:
crontab -e
0 2 * * 0 /home/adam/restic-backup.sh >> ~/restic-backup.log 2>&1


lorem ipsum dolor

# NAS On-The-Go

## Install Tailscale
lorem ipsum dolor
[install Tailscale](https://tailscale.com/download/linux/rpi)

lorem ipsum dolor
[tailscale pi setup](https://pimylifeup.com/raspberry-pi-tailscale/)
