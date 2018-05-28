# Rockster
A rhythm game prototype for Gamebuino Meta with custom track support.

By: Dark Archon, arhn.eu

Graphics: Neko

Tracks charted by: Kicaken & Wielkimati

## Please note: while the game source code is free to use, share and edit, the included music tracks are mostly copyrighted content used with EXPLICIT permission from the musicians. The tracks are protected by copyright laws and can ONLY by shared as part of the game bundle.

This game will currently NOT WORK with Gamebuino Meta emulators due to lack of sound and image loading support.
A simple Windows port is planned for the near future to allow PC users to try the game out locally.
Please let me know if you can help out with compiling it for Windows!

This is a prototype and a very early work in progress version of Rockster -- a sample rhythm game for Gamebuino Meta.

## Features
A simple rhythm game with a score and points multiplier counter. Press A and B to match the falling arrows to the music playing in the background.
The game was written mostly to utilize the amazing LEDs on Gamebuino Meta and SD card access feature.
Features:
- custom tracks support via SD card upload
- a simple browser based editor for creating custom tracks
- cover art support for displaying album art in the song selection menu
- song credit support for custom tracks

While the game is currently playable at a very basic level:
- custom song selection and cover art works
- the game can be played, score updates and the basic functionality exists

...it is still far from completed.
To-do:
- make tracks finishable. Currently notes stop updating at around 2:13 due to memory constraints. Will fix in next version.
- currently songs don't end when the track is over
- many minor and major bugs need fixing
- proper game modes to be added
- covers stop working after quitting a song using the "Menu" key.
- Error detection. Currently the game will crash if there are no songs loaded or there are issues with song formats.
- palletes need to be fixed for the low-color mode
- graphics need to be redesigned to make chords more visible
- interface needs polishing
- game needs to be more game-y
- proper LED support for a more concert-like experience
- custom background and note support for tracks

## How to use:
The game currently DOES NOT work in Gamebuino Meta emulators!
1. Copy the .bin file and the MUSIC directory into /rockster folder on SD root.
2. Music tracks inside are optional and can be freely replaced / deleted as deemed necessary.
3. The game will currently crash if there are no songs or the song format is incorrect (read below for details).
4. Instructions for creating your own tracks are located below.
5. The game is currently just proof of concept so while you can play your music, songs over 2 minutes will crop out. There isn't an ending screen anywhere yet and the game tends to be quite glitchy. Use the "MENU" button to quit a song.

## Controls:
Game controls:
Press A to "hit" the red arrow, B to "hit" the blue arrow. For chords (both notes pressed at the same time) LEFT on the d-pad can be used instead.

Editor controls:
Open the editor in your favourite browser. Load a song, press play and use A, S and D to "create the notes". This is currently very basic but good enough for the prototype.

## Creating custom tracks:
1. Create a note track as described above. Copy the track contents and save as [trackname].txt.
2. Convert your music file to an 8-bit unsigned wav file with a bitrate of 44.1kHz (max. sound frequency of 22050Hz)
- play around with the settings, I had issues with stereo files playing to slow on the Meta unless converted to mono (?) - not sure what the problem there was
3. Save the music file as [trackname].wav
4. Create a cover file and save it as a bitmap file named [trackname].bmp. The file needs to be 80x64 pixels and either 16 or 24-bit depth.
5. Create a credits file and fill it with any information, using the pipe (|) symbol for line-breaks. Save it in [trackname].cre format.
6. Copy the files to the /rockster/music/ folder on the SD card.

## Song credits:
Included with the game as an optional download and stored in the /music folder are 13 songs. They are included here with permission from original creators. Some of the tracks are not normally available for free and are commercial tracks and as such cannot be shared or distributed without the game. I know it's weird, but copyrights are bizarre like that.

The included tracks are as follow:

Beyond the Hatred
By: As Night Falls
Album: Embrace the Journey
Year: 2016
WWW: asnightfalls.bandcamp.com

Believe
By: Marcin "Esperar" Procek

Blaze
By: BarthuS & Goradios
Year: 2012
WWW: soundcloud.com/goradios

DREAM/BURST
By: hitmod
Year: 2018
WWW: ?

Echiko
By: Chip Jockey
Album: Arcade Trip
Year: 2017
WWW: chipjockey.bandcamp.com

Nothing to Lose
By: Escape Control
Album: Dworek DEMO
Year: 2017
WWW: facebook.com/escapectrl

Fast and Dumb
By: MR M8
Album: 4LBUM
Year: 2017
WWW: soundcloud.com/mr-m8

NESMania Chiptune
By: Ben Burnes aka Abstraction
Year: 2016
WWW: soundcloud.com/abstraction

On The Stage Tonight
By: DJ Hard
Album: -
Year: 2017
WWW: jamendo.com/artist/367586/dj-hard

She's Gone Mad
By: Rooster Cock
Year: 2018
WWW: soundcloud.com/roostercock

Turnin' To It
By: S-AGE
WWW: s-age.pl

Timbo
By: Goradios
Year: 2012
WWW: soundcloud.com/goradios

Wobble
By: Arkadiusz Stawicki

More tracks coming soon!

## Extra libraries used:
The song editor uses the free Jquery (https://jquery.com/) and Wavesurfer (https://wavesurfer-js.org/) javascript libraries.
