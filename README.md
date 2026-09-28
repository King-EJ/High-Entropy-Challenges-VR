# High-Entropy-Challenges-VR
VR Mod High Entropy Challenges

HIGH ENTROPY VR  -  VR mod for "High Entropy: Challenges" (Unity 2022.3.62f2 Mono x64)
=======================================================================================

Version 0.1.5 (test build on Quest 3).

WHAT IT DOES
------------
* Full stereo VR through OpenXR (SteamVR, Meta/Oculus, Virtual Desktop, WMR...).
* You look around with your head; the game's own camera follows your headset.
* Point at doors, items and switches with your right controller to use them (blue pointer).
* The first-person weapon (with its arms) is moved to your VR hand. Bullets, bolts and melee go
  where the gun points. A laser sight shows while you aim (left trigger).
* Your VR controllers appear to the game as an Xbox-style gamepad, so every menu, the inventory,
  the weapon wheel and computer screens work exactly like with a controller - and you can remap
  buttons in the game's own Options > Controls > Gamepad screen.
* HUD and menus are shown on a floating screen (can also be held on a hand).
* Controller vibration comes from the game's own gamepad rumble.

INSTALL
-------
1. Copy EVERYTHING in this zip into the game folder (next to the game's .exe),
2. Start SteamVR (or your OpenXR runtime), then launch the game.
3. In the game's options, set the input device to Automatic (or Gamepad), not Keyboard/Mouse.
   

CONTROLS (right-handed default = Xbox layout on Quest-style controllers)
--------------------------------------------------------------------------
(controls can be change in game to your liking)

Right trigger ........ RT  Fire

Left trigger ......... LT  Aim / zoom 

Right grip ........... RB  Reload (shows the laser)

Left grip ............ LB  Grenade

A .................... A   Jump / confirm

B .................... B   Crouch / back

X .................... X   Interact (I change to B in game settings)

Y .................... Y   Secondary interact

Left stick ........... Move        (click = L3 Run (I change to LT in game settings), hold = START game menu)

Right stick L/R ...... Smooth turn   (in menus: right stick)

Right stick up/down .. D-pad up / down (night vision / medkit)

Right stick click .... tap = D-pad left (weapon wheel), hold = SELECT (inventory)

Both stick clicks .... Re-centre the view

(What each pad button does is the game's own gamepad mapping.)

CONFIG  -  BepInEx\config\hec.vr.cfg  (created on first launch, edits apply live)
---------------------------------------------------------------------------------
[GamepadMapping]  which VR control presses each pad button, e.g.  Start = OffStickClick:hold
                  (MainX = gun hand, OffX = other hand; :tap / :hold for short / long press)
                  
[Weapons]         AimRotationOffset, GunModelRotationOffset / GunModelPositionOffset (move the
                  weapon in your hand), LaserRotationOffset, LaserSight, BarrelLength,
                  AimWithHand, WeaponInHand, LaserButton (which pad button shows the laser)
                  
[Interaction]     InteractWithHand (use/pick up what the controller points at), Hand, ShowPointer

[Weapon.<name>]   created automatically for each weapon - per-weapon versions of the offsets

[Camera]          EyeHeightOffset, AnchorSmoothing, IncludeHelmetCamera, CopyCameraEffects ...

[UI]              FollowMode (Lazy / Head / GunHand / OffHand), Distance, Width ...

[Cheats]          UnlimitedHealth



CREDITS & LICENCES
------------------
* High Entropy: Challenges belongs to its developer Álvaro García (binarynonsense).
* OpenXR.dll (native OpenXR bridge) by Astien (c) 2025 - free, non-commercial redistribution,
  see BepInEx\plugins\HECVR\LICENSES. This mod must stay free.
* BepInEx - LGPL 2.1. This is a fan-made, non-commercial mod.
