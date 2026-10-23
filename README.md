# Deadlock x10 - Server Kit

This kit runs a Deadlock x10 server on your PC. Friends join through Steam,
no port forwarding needed. You get everything the mod can do, including the
server-only parts (Solomon 11 bishops, Mirage/Apollo 10 recasts, 3s respawn,
CC protection, heroes deal 65% less damage to objectives ...).

Requirements
1. Windows 10/11, Deadlock installed through Steam
2. .NET Runtime 10 (x64): https://dotnet.microsoft.com/download/dotnet/10.0 (setup checks it)
3. Deadworks (server plugin loader), Windows release zip: download it from the
   Deadworks release page and put the zip in this folder (not included in this kit)

First time
1. Unzip this kit anywhere
2. Put deadworks-....zip in the same folder
3. Close Deadlock, then double-click  setup_server.bat
   It finds Deadlock, installs Deadworks, the x10 plugin and the x10 mod (unless
   Deadlock Mod Manager already installed it) and adds 2 lines to gameinfo.gi so
   friends can join over Steam (backup: gameinfo.gi.before_x10)

Start the server
1. Double-click  start_x10_server.bat  and wait until the map has loaded
2. You: Deadlock -> Settings -> enable "Dev command console", press F7:
   connect localhost:27016
3. Friends: type  status  in the SERVER window, copy the steamid
   (e.g. [A:1:1234567890:12345]); friends press F7 and type
   connect [A:1:1234567890:12345]     (it changes on every server start)
4. Everyone should install the same x10 mod version, otherwise tooltips and
   range indicators show normal values (the real values are still x10)

Settings: Deadlock\game\bin\win64\configs\X10ServerPlugin\X10ServerPlugin.jsonc
After editing, type  dw_reloadconfig  in the server window. Setup never
overwrites it: delete it and run setup again to get the defaults back.

After a game update: run setup_server.bat again. If Deadworks does not support
the new game version yet, wait for a Deadworks update.

