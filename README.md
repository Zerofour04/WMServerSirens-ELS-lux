
# 🚨WMServerSirens - Server Sided Sirens

## Hey, I integrated Server Sirens in this resources, just download it:
### - [Lux_vehcontrol-Version](https://github.com/Zerofour04/lux_vehcontrol-WMServerSirens)
### - [ELS-Version](https://github.com/Zerofour04/ELS-FiveM-WMServerSirens)

We’ve only gone and done it! Ladies and gentleman, after many strenuous hours of hard work, we’ve finally developed server side sirens for FiveM! We’ve seen a constant demand for this resource and that’s given us a huge motivational boost to develop it. You can now add server side sirens to your server which can be used in conjunction with a majority of siren scripts (eg. luxart). You can also change the air/bullhorn!

This documentation will assist with the installation of sirens and provide a starting point for developers, configuring the plugin for use with their ELS scripts.

## 🔧Installation
1. :Download the resource from GitHub [here](https://github.com/Walsheyy/WMServerSirens).
2. : Copy ‘wm-serversirens’ to your resources folder.
3. : Open your server.cfg and write“ensure wm-serversirens” anywhere in the config.
4. : Follow our documentation on adding custom sirens below!
  
## 🔊Adding custom sirens
We’ve provided the ability for you to add custom sirens without any knowledge of code or development. After following our simple guide, you’ll be cooking on gas in no time!
You’ll be required to use OpenIV or another AWC editing program to add or edit custom sirens into the game. Our plugin comes ready with 3 siren pack AWC files ready to edit.

1. : Navigate to “dlc_wmsirens” in the directory.
2. : Navigate to the “oac” folder.
3. : Change the .wav files with your custom .wav files. Do not change the file names, this is very important, WMServerSirens will not function properly if you do this.
4. : After editing the siren pack, navigate to the .oac file and drag it into OpenIV. This will compile the .AWC file together and allow you to use it in your server.
5. : Drag and drop the AWC file you previously created into “dlc_wmserversirens”, replacing the base siren pack. Do not change the name of the siren pack.
6. : Start up your server and go for a celebratory drive! Let off some fireworks.

In there, you’d change VEHICLES_HORNS_SIREN_1, with “SIREN_ALPHA”. However, you would need to edit the ELS script to use the “DLC_WMSERVERSIRENS_SOUNDSET”  custom DLC when playing the sound from the entity.

On the other hand, you could use an if statement in code, checking the current vehicle and then play the right siren.

**Naming convention:**

As you may notice, the sirens you’ll be editing are all named using the phonetic alphabet, this will be used to keep track of the siren number for our development purposes.

A quick google search will reveal the full list of the alphabet for you.

## 🆘Support
LONDON STUDIOS DISCORD - Join [HERE](https://discord.gg/F2zmUTD).
WALSHEY MODIFICATIONS DISCORD - Join [HERE](https://discord.gg/uVuW5Am).
[Video on how to install](https://youtu.be/ZgZT_TuMdbU "How to install Server Sided Sirens for FiveM")

### Feedback and suggestions
We thank you for downloading this resource, we've worked extremely hard on it and we hope you enjoy using it. However, we will always be looking for feedback and suggestions in the comments below.

We'd like to credit Double Doppler for his British sirens, included in the resource.

## 🛠️Requesting the audio:
At the top of your ELS script, you’ll need to request the audio for the custom sirens, essentially downloading it for all clients, as these are external sounds.
`RequestScriptAudioBank(“DLC_WMSIRENS\\SIRENPACK_ONE”, false)`

If you’ve only made changes to the first siren pack, you’ll only need to include the first one.

**Playing the custom sounds:**
To play a siren from a vehicle, use the following native:

PlaySoundFromEntity(-1, “SIREN_ALPHA”, veh, “DLC_WMSIRENS_SOUNDSET”, 0, 0)

“veh” = The vehicle the player is in, we recommend using GetVehiclePedIsUsing(PlayerPedId()).

**Example:**

<ManTone1 AllowUse="true" AudioString="VEHICLES_HORNS_SIREN_1" />
