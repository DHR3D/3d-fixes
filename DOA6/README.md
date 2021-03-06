Dead or Alive 6
===============

**NOTICE: The installation for this game is different to our other mods -
please read below!**

Installation
------------
1. Extract the zip file to a directory of your choosing, but **DO NOT extract
   to the game directory** (the game will shut down after the splash screen if
   you extract it to the game directory).

2. Run the "3DMigoto Loader.exe"

3. The loader will launch the game through Steam automatically.

4. **Once in game, press F7 to switch to exclusive full screen and engage 3D
   Vision.**

Keys
----
- F7: Switch to exclusive full Screen mode to enable 3D Vision
- XBox controller back button: Take 3D screenshot (saved to
  Documents\NVStereoscopic3D.IMG, same as Alt+F1, but without the message)

Fixed
-----
- Fix detached body parts (full regex based replacement for the 3D Vision
  stereo correction and driver heuristics)
- Regex halo fix
- Lights & shadows
- Decals (tiled decals)
- Accurate specular highlights (these take the game from an 8 to an 11 IMO)
- Tweak main menu background and character placement
- Water & reflections
- Volumetric fog light shafts (A.P.O. stage. They look a bit naff, but that's
  true in 2D as well)
- Synchronised plant breeze physics between both eyes
- Treasure room coin spawners
- Graphical glitches in the treasure room
- Clouds, sun & flares
- Hides hardware mouse cursor
- Story mode cutscenes render in both eyes in SLI (mono video is still mono)
- In game screens in the Colosseum and Muscle stages are converted to mono
  screens to avoid violating infinity and stereo inversions. If you prefer the
  gimmick of having a 3D screen inside a 3D screen (inside a 3D screen, inside
  a 3D screen...) and don't mind straining your eyes to see what lies beyond
  infinity, edit the d3dx.ini and change $mono_in_game_screens to 0 under
  [Constants]

ReShade Compatibility
---------------------
3DMigoto can be used to load ReShade into DOA6 if you like (please note:
ReShade is *NOT* provided with this download). To do this, edit the d3dx.ini
and uncomment (remove the semicolon) the line that reads:

    proxy_d3d11=reshade.dll

Rename ReShade's dxgi.dll to reshade.dll and place all the files that it uses
in the same directory where you extracted this mod. Run the 3DMigoto Loader.exe
and the game should launch with both 3DMigoto and ReShade loaded.

If you are not using the 3D Vision part of this mod, consider disabling it for
better performance. In the "Mods" directory you will see a "3d-vision" folder -
delete this or rename it to "DISABLED 3d-vision".

Side-by-Side / Top-and-Bottom Output Modes
------------------------------------------
This fix is bundled with the SBS / TAB output mode support in 3DMigoto. To
enable it, edit the d3dx.ini, find the [Include] section and uncomment (remove
the semicolon) the line that reads:

    include = ShaderFixes\3dvision2sbs.ini

Then, in game press F11 to cycle output modes. If using 3D TV Play, set the
nvidia control panel to output checkerboard to remove the 720p limitation.

Known Issues
------------
- Occasionally 3D may be disabled after loading the main menu (possible driver
  bug?). Double check you are in full screen and restart the game (via
  "3DMigoto Launcher.exe") if this happens.
- If the game closes down by itself just after the spash screen, make sure you
  have not installed the fix into the game directory. Use the provided
  uninstall.bat to remove it if you put it there by mistake.

Like my Work?
-------------
Fixing games takes a lot of time and effort, and I also do a lot of work on
3DMigoto behind the scenes to make all of these mods possible - in particular,
this release required writing an entirely new loader mechanism for 3DMigoto as
well as solving a lot of hangs and crashes.

If you are in a position where you are able to do so, please consider
[supporting me with a monthly donation on Patreon][1], and thanks again to
those that already do! While I prefer the more stable monthly support that
Patreon offers, I can of course understand that some of you prefer to make
one-off donations when you can, and for that you can use [my Paypal][2]. As a
reminder, these donations are to support me personally, and do not go to other
modders on this site.

[1]: https://www.patreon.com/DarkStarSword
[2]: https://www.paypal.me/DarkStarSword

_This mod is created with 3DMigoto (primarily written by myself, Bo3b and
Chiri), and uses Flugan's Assembler. See [here][4] for a full list of
contributors to 3DMigoto_

[4]: https://darkstarsword.net/3Dmigoto-stats/authors.html
