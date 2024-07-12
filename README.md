M8C for ArkOs - this an updated/modified version of Metro Grade's 1M8ARK.zip that works with M8 version 4.0

M8 v4.0 has some changes that cause it to not work properly with earlier vesions of laamaa's M8C.   



How to install:

Existing Users:  If you already had M8c set up on you ArkOs device and just need to upgrade M8C to the current build for M8 4.0, all you need to do is replace your existing _m8c folder with the one here.   thats it.   

New Users:  If you are installing M8C on your ArkOs device for the first time; download the entire repository, (unzip it,) and rename it to "m8" (lowercase).  Put this in your "roms" directory (or roms2 if you are using the 2nd card.) Next, enable wifi and remote access in arkos "options".   Using  "file manager" (also in "options") find the m8->setup folder and run the setup.sh script.   

If you would like to add M8 to emulationstation's game system listings so m8 appears as its own "game system"  alongside NES, sega, etc, with all your m8c launch scripts, midi detect etc listed like game roms:    open /etc/emulationstation/es_systems.cfg  
        
        nano /etc/emulationstation/es_systems.cfg       

and then, add this bit at the end,  just before the </systemList> line  at the bottom
   
           <system>
            <name>m8</name>
            <fullname>M8 Tracker</fullname>
            <path>/roms/m8</path>
            <extension>.sh</extension>
            <command>%ROM%</command>
            <platform>ignore</platform>
            <theme>m8</theme>
          </system>

