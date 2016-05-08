script.service.BR_iso-Enhancements
==================================

Kodi add-on, needs Helix as minimum

Install:
========
Download: Right-click on "script.service.BR_iso-Enhancements_vx.x.x.zip", select "Save Link As...".

Rename "script.service.BR_iso-Enhancements_vx.x.x.zip" to "script.service.BR_iso-Enhancements.zip"

In Kodi: System / Settings / Add-ons / Install from zip file  -> select "script.service.BR_iso-Enhancements.zip"

Usage:
=======
You need to know what playlist you want to play from the bluray.

eg:

Bluray contains a theatrical cut (playlist 800), and a directors cut (playlist 801).

To play the theatrical cut, rename the iso to: "movie X (year).Bluray.PlayList[00800].iso"

To play the directors cut, make a new dir in you NAS, name it movie x - dir cut, and put a hardlink
in this dir, pointing to the "movie X (year).Bluray.PlayList[00800].iso" file. The name of this hardlink should be:
"movie X (year) - dir cut.Bluray.PlayList[00801].iso"

eg:

Bluray with 5 episodes, each epsiode is a playlist (ep1 = 50, ep2 = 51, ep3 = 52, ep4 = 53, ep5 = 54).

ep1: Make a hardlink to the iso, name the hardlink: "tv-show.s01e01.PlayList[00050].iso"

ep2: Make a hardlink to the iso, name the hardlink: "tv-show.s01e02.PlayList[00051].iso"

ep3: Make a hardlink to the iso, name the hardlink: "tv-show.s01e03.PlayList[00052].iso"

ep4: Make a hardlink to the iso, name the hardlink: "tv-show.s01e04.PlayList[00053].iso"

ep5: Make a hardlink to the iso, name the hardlink: "tv-show.s01e05.PlayList[00054].iso"

eg:

Bluray with 5 episodes, each epsiode is a playlist (ep1 = 50, ep2 = 51, ep3 = 52, ep4 = 53, ep5 = 54). You don't want to see the (previously on... recap)

ep1: Make a hardlink to the iso, name the hardlink: "tv-show.s01e01.PlayList[00050-00_01_02].iso" skips first 62 seconds of the show

ep2: Make a hardlink to the iso, name the hardlink: "tv-show.s01e02.PlayList[00051-00_00_52].iso" skips first 52 seconds of the show

ep3: Make a hardlink to the iso, name the hardlink: "tv-show.s01e03.PlayList[00052-00_00_58].iso" skips first 58 seconds of the show

ep4: Make a hardlink to the iso, name the hardlink: "tv-show.s01e04.PlayList[00053-00_01_00].iso" skips first 60 seconds of the show

ep5: Make a hardlink to the iso, name the hardlink: "tv-show.s01e05.PlayList[00054-00_00_44].iso" skips first 44 seconds of the show

eg:

Bluray with 5 episodes, all episodes are in 1 big playlist (duration is about 3h45m) (ep1 = 50, ep2 = 51, ep3 = 52, ep4 = 53, ep5 = 54).

ep1: Make a hardlink to the iso, name the hardlink: "tv-show.s01e01.PlayList[00050=00_00_00=00_45_00].iso" First 45 minutes is episode 1

ep2: Make a hardlink to the iso, name the hardlink: "tv-show.s01e02.PlayList[00051=00_45_01=01_30_00].iso" Second block of 45 minutes is episode 2

ep3: Make a hardlink to the iso, name the hardlink: "tv-show.s01e03.PlayList[00052=01_30_01=02_15_00].iso" third 45 min block is episode 3

ep4: Make a hardlink to the iso, name the hardlink: "tv-show.s01e04.PlayList[00053=02_15_01=03_00_00].iso" Fourth 45 min block is episode 4 

ep5: Make a hardlink to the iso, name the hardlink: "tv-show.s01e05.PlayList[00054-03_00_01].iso" Last block is episode 5
