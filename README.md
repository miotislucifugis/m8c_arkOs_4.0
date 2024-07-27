# M8C 1.76 for ArkOs2.0 - 
### this an updated/modified version of Metro Grade's 1M8ARK.zip that works with M8 version 4.0

lamaa's M8C (https://github.com/laamaa/m8c) can be a little trick to get running on ArkOS. Fortunately discord user, Metro Grade, made a really nice and helpful zip with a prebuilt version of M8C and a bunch of useful scripts, though due to some changes in M8 v4.0, this build of M8C no longer works (screen glitches) and needs to be updated to the newest version.   Since updating m8c directly on stock ArkOs can be sort of a pain, I thought Id update his origial work.



## How to install:

Existing Users:  If you already had M8c set up on you ArkOs device and just need to upgrade M8C to the current build for M8 4.0, all you need to do is replace your existing _m8c folder with the one here.   thats it.   

New Users:  If you are installing M8C on your ArkOs device for the first time; download the entire repository, (unzip it,) and rename it to "m8" (lowercase).  Put this in your "roms" directory (or roms2 if you are using the 2nd card.) Next, enable wifi and remote access in arkos "options".   Using  "file manager" (also in "options") find the m8->setup folder and run the setup.sh script.   Reboot.  Plug in your teensy flashed w/ m8 headless and return to m8 folder (again w/ file manager) and run the m8.sh script.  M8c should launch.


### Configure the quit button

R33s & R36s users: To be able to quit m8c and return to emulation station, you may need to change the "quit" button number to "9" in config.ini (9 = L1 on R33s) .... (or use whatever button you want.) 

                nano home/ark/.local/share/m8c/config.ini

this enables quitting by pressing "L" and "select".


 ## EXTRA:


If you would like to add M8 to emulationstation's game system listings so m8 appears as its own "game system"  alongside NES, sega, etc, with all your m8c launch scripts, midi detect etc listed like game roms:    open /etc/emulationstation/es_systems.cfg  
        
        nano /etc/emulationstation/es_systems.cfg       

and then, add this bit at the end,  just before the ```</systemList>``` line
   
           <system>
            <name>m8</name>
            <fullname>M8 Tracker</fullname>
            <path>/roms/m8</path>
            <extension>.sh</extension>
            <command>%ROM%</command>
            <platform>ignore</platform>
            <theme>m8</theme>
          </system>

(change the path to "roms2" if necessary.)   Restart EmulationStation.   Afterward, M8 will be one of the gamesystem listing.


Thanks to laamaa for M8C - https://github.com/laamaa/m8c , Metro Grade for the original 1M8Ark.zip,  and of course, Dirtywave/ trash80 for generously creating m8 headless for us all to try out, gratis!  if you enjoy m8 headless, please buy a real m8, its worth it!   https://dirtywave.com/
