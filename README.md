# Volkswagen RNS315/RNS310 mmc_tools
* Tested on Volkswagen Passat B7 w/ RNS315
* (might work on other non-VW cars?)
* Built from Linux sources / Compiled for amd64
* Should also work on Skoda/Seat/Audi with similar navs

This is a tool that lets you turn Generic SD Card/Samsung EVO card to be recognized by the RNS as a Map Update card.
You must start with a FAT32 card, containing the navpsf_update folder

#### Usage:
* Working on Linux 4+ compatible systems
* Tested on openSUSE Thumbleweed and Ubuntu LTS
```
$ git clone https://github.com/TudorGruian/vw_mmc-tools.git
$ cd vw_mmc-tools
$ chmod +x mmc
# and after that you can use ./mmc command, you have to read forums depending on your nav system.
```
# Updating the maps on RNS315 (THIS GUIDE IS FOR RNS315 ONLY, IF YOU DON'T HAVE THIS NAVIGATION, YOU MIGHT END BREAKING YOUR SD CARD, IF YOU HAVE OTHER SYSTEM, SUCH AS RNS310 READ OTHER FORUMS)

Steps:
Extract the content and copy on the SD, top folder is navpsf_update
Look under /dev  to see which SD is yours, in my case it is mmcblk0

Change the CID with the attached tool
sudo ./mmc prog_cid /dev/mmcblk0 5d53424c32424d31013917ca53010400
remove the card and reinsert it

Now lock the card by password, it's not possible to unlock it with normal MMC
driver, you need a patched version of kernel to be able to unlock it. Password
you know from command below.
sudo ./mmc lock_sd /dev/mmcblk0 C99A20843ED7D90B6801E49F2BC80277

Enjoy your new maps!
