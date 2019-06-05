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
