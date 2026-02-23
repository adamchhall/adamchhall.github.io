+++ 
draft = true
date = 2026-02-22T20:12:41-05:00
title = "Setting up my Raspberry Pi NAS"
description = ""
slug = ""
authors = [ "Adam Hall"]
tags = []
categories = []
externalLink = ""
series = []
+++

# Raspberry Pi NAS: A First Step towards Digital Freedom
lorem ipsum dolor

Any version of the Raspberry Pi Imager less than 2.0.0 seems to fail to write settings appropriately to 
the flashed SD card, resulting in endless headaches when trying to connect to a Pi with a headless configuration
via wifi! Becuase the WiFi password and SSID have not been correctly configured, the device will immidiately and
silently fail to connect to the Internet if this isn't addressed. Your options are to make sure you are using a
very recent version of the Pi Imager, to plug the Pi into a monitor and keyboard to configure it even if you plan
to eventually run it headless, or to find the correct config files to change these settings manually after the
image is flashed.

Once this initial hurdle is out of the way, it is fairly easy to follow the instructions from this
[tutorial](https://www.hackster.io/ElecrowOfficial/diy-nas-network-attached-storage-with-raspberry-pi-5-e91a37)
to get a basic [NAS](https://en.wikipedia.org/wiki/Network-attached_storage) working.

lorem ipsum dolor
[install Tailscale](https://tailscale.com/download/linux/rpi)

lorem ipsum dolor
[tailscale pi setup](https://pimylifeup.com/raspberry-pi-tailscale/)

to find uuid: "sudo blkid"
make directory /mnt/data/
in fstab add "uuid=whatever /mnt/data btrfs defaults,nofail 0 2" at the bottom

install syncthing
sudo apt install syncthing
