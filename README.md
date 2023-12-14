# Thief on Linux Guide for Steam Version

This guide is assembled from various sources to assist enthusiasts (taffers) in setting up Thief and Thief 2 on their Linux PCs. It is specifically tailored for the Steam version of the game.

## Prerequisites

- Ensure that Steam is installed and set up on your PC.

- Install `wine` by following the guide : <https://wiki.winehq.org/Wine_Installation_and_Configuration>

- Configure Steam to use Proton `7.0-6`

## Setting Up Thief and Thief 2

1. Install the game on Steam as you would with any other game.
2. Confirm that you are targeting Proton version `7.0-6` in your Steam settings or enforce it for the game.
3. Download the patches from the following threads:
   - Thief 1/Gold: [Thief 1/Gold Patch](https://www.ttlg.com/forums/showthread.php?t=134733)
   - Thief 2: [Thief 2 Patch](https://www.ttlg.com/forums/showthread.php?t=149669)

4. Use `wine` to run the downloaded patch installer from the ttgl website.
   - For example you could run this command : `wine T2Fix.exe`
   - This will launch the installer like it would on a Windows PC.
   - In the installer, navigate to your Thief installation directory.
   - If the folder starts with a `.` and is hidden, locate it in a terminal and copy the path into the setup.
     - Thief Gold: `[/home/{yourname}/.local/share/Steam/steamapps/common/thief_gold)`
     - Thief 2: `[/home/{yourname}/.local/share/Steam/steamapps/common/thief_2)`

5. Once the setup is over, try running the game for the first time and address any issues that may arise.
6. Adjust keybindings as needed in the game options.
7. Be mindful of potential mouse acceleration issues caused by your OS settings.

## Preparing Your Home Directory for Fan Missions

Create folders that will be utilized by AngelLoader to load your Fan Missions.

```bash
cd
mkdir thief_fm
mkdir thief_bak
```

`thief_fm` will be the folder to drop any fm `.zip` file.\
`thief_bak` is used by AngelLoader to prevent you from breaking your thief game.

## Setup AngelLoader

This setup might not be optimal, but it offers an enjoyable way to keep recording your playtime on Steam.

- Download the latest release from : <https://github.com/FenPhoenix/AngelLoader>
- Now into your game folder and backup the main `THIEF.exe` file into something else. Ex : `THIEF_GAME.EXE`
- Extract the `AngelLoader` zip into the game folder and rename the `AngelLoader.exe` file into `THIEF.EXE`
- Now you can launch `AngelLoader` from Steam directly by starting the game.
- Setup `AngelLoader`` with the right paths.
  - Thief 1 Path : `Z:\home\{yourname}\.local\share\Steam\steamapps\common\thief_gold\THIEF_GAME.EXE`
  - Fm folder: `Z:\home\{yourname}\thief_fm`
  - backup: `Z:\home\{yourname}\thief_bak`
- If you add the thief 2 game path, you'll be able to launch some thief 2 FM from AngelLoader
- Test by downloading Fan Missions and copying the zip files into your `thief_fm` folder that we created previously.

## Thanks

I hope this guide I wrote in 5 min can help you enjoy thief on your Linux PC 😀
