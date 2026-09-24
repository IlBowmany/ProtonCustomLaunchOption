# Proton Custom Launch Option

Hi!

You are looking for a simple way to launch alternative exe using Proton, through Steam, without having to resort to ProtonTricks/SteamTinkerLaunch/etc.?
Say no more!

You just need to open your Steam game propriety, and in launch option write this command:

> echo "%command%" | sed 's/ORIGINALEXE/ALTERNATIVEEXETOLAUNCH/' | sh (This works on Debian)

or

> eval $(echo "%command%" | sed s/ORIGINALEXE/ALTERNATIVEEXETOLAUNCH/) (This works better on Fedora and Arch)


For example, here is how to launch the Dark Souls III Seamless Mod with this command:

> echo "%command%" | sed 's/DarkSoulsIII.exe/ds3sc_launcher.exe/' | sh

Or here is how I launch the F4SE for Fallout 4:

> echo "%command%" | sed 's/Fallout4Launcher.exe/f4se_loader.exe/' | sh

Both exes must be in the same folder! So if you have to launch an exe somewhere else, I would reccomend you to write an echo bash script in bat that pinpoint the exe and link it.


Hope you enjoyed the guide! Happy gaming :D
