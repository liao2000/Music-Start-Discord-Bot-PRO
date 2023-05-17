# Music Start Pro

[![NPM version](https://img.shields.io/npm/v/music-start-pro.svg?logo=npm&style=flat-square)](https://www.npmjs.org/package/music-start-pro) ![](https://img.shields.io/github/license/ksw2000/Music-Start-Discord-Bot-Pro?style=flat-square) ![](https://img.shields.io/github/stars/ksw2000/Music-Start-Discord-Bot-Pro?style=flat-square) ![](https://img.shields.io/github/issues/ksw2000/Music-Start-Discord-Bot-Pro?color=yellow&style=flat-square) [![](https://img.shields.io/discord/864220336841162756?style=flat-square)](https://discord.gg/qQM9avGy2R) ![](https://img.shields.io/npm/dt/music-start-pro?color=blue&style=flat-square)

![](https://i.imgur.com/I1cH4Uc.png)

## Overview

Music Start Pro is a discord bot that can play YouTube music by slash command.

```sh
# Install
npm install -g music-start-pro

# Start music-start-pro
ms --token [YOUR-DISCORD-BOT-TOKEN]

# See help
ms --help
Usage: ms [options]

Options:
  -v, --version                    output the current version
  -t, --token <discord_bot_token>  specify the discord bot token (default: "")
  -d, --disable-log                do not save and load the log file
  -h, --help                       display help for command
```

Get token on [Discord Developer Portal](https://discord.com/developers/applications)

Add the bot to your Discord server by visiting

```
https://discord.com/api/oauth2/authorize?client_id=[YOUR-CLIENT-ID]&permissions=8&scope=bot%20applications.commands
```

> **Notice** 
>
> You must run `music start bot` server before joining the bot to the Discord guild.

---

+ [Click here to invite testing bot to your guild.](https://discord.com/api/oauth2/authorize?client_id=889377515225886800&permissions=8&scope=bot%20applications.commands) The availability of the server is not guaranteed.
+ [Join our Discord server.](https://discord.gg/qQM9avGy2R)

## Features

+ `/attach` 
  + Attach MS Pro to the voice channel where you are. Thus, you must join in the voice cannel first.
  + At the same time, the command fetch the new instructions set if updated.
  + You can detach the MS Pro by `/detach`.
  + If you move the MS Pro to another voice channel, please type `/attach` again after move.
+ `/append [youtube-url]`
  + Append the song into the playlist by given YouTube URL.
  + You can just input the video id. That is, if you want to play `https://www.youtube.com/watch?v=Qj0Dmwxv-KY`, you can just `/append Qj0Dmwxv-KY`
+ `/lang [code]`
  + Now support `en` and `zh`
  + en: English
  + zh: Traditional Chinese
+ Playlist
  + `/list` Show the playlist.
  + `/swap [idx1] [idx2]`Swap 2 song by index number.
  + `/remove [idx]`Remove song by index number.
  + `/clear` Remove all songs.
  + `/sort` Sort the playlist in alphabetical order. 
  + `/shuffle` Shuffle the playlist.
  + `/distinct` Remove duplicate songs.
+ Player control
  + `/jump [idx]` Jump to a song in the playlist by given index.
  + `/pre` Play the previous song.
  + `/next` Play the next song.
  + `/vol` Show the volume.
  + `/vol [number]` Set the volume, where number is in [0, 1]
  + `/pause`, `/resume`, `/stop`
+ Batch Operation
  + `/json` Output the playlist by json format
  + `/json [json-string]` Add a batch of songs by given a json string
  + `/aqours` Append Aqours' songs that author recommends into playlist.
  + `/llss ` Add all the songs about LoveLive Sunshine into playlist. The list is provided by Benny.
  + `/azalea` Add AZALEA's songs that author recommends into playlist.
  + `/muse` Append some μ's' songs into playlist.
  + `/nijigasaki` Append some 虹ヶ咲's songs into playlist.
  + `/liella` Append some Liella' songs into playlist.
+ General index number
  + The index is start at 0
  + Negative number -1 stands for the last song
  + Support overflow, e.g., we have 16 songs
    + The first song 0 = 16
    + The second song 1 = 17
    + The last song 15 = 31 = -1 

![](https://i.imgur.com/lkvXj34.png)

## Develop

```sh
# clone the repository
git clone https://github.com/ksw2000/Music-Start-Discord-Bot-Pro

# initialize
npm i

# start the program by
npm run start

# please use lint before making a pull request
npm run lint
```