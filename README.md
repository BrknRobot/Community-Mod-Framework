# Community-Mod-Framework
Framework mod to support compatibility between including GUI, Political Movements, Parties and mod detection triggers

## Political Movements ##

Overwrites vanilla Political Movement definitions with scripted triggers to aid in mod compatibility

Add dummy ideologies from mods into political movements, allowing them to spawn with the appropiate mod enabled:
* Add a dummy ideology with the same name as your mod ideology
* Assign the ideology to the appropiate political movements (and scripted triggers if needed)
* Load this mod below any other mod
* Your mod will overwrite the ideology definition and allow it to spawn in the specified political movements

## GUI Framework ##

Current Scope:
1) A "sidebar" scripted widget to deconflict mods that want to add custom sidebar buttons. (Done in cooperation with LordR)
2) Modification to the GUI template fullscreen_hide to hide the outliner whenever a scripted widget window is open. (Already done by myself)
3) Modification to objective_types to add a scrollbar to the objectives screens. (Credit to KarafuruAmamiya and Xier)
4) Integration of the "Modded DLC Framework" (Credit to 1230James)
5) Unified system for cooltip types (Credit to 1230James)
6) Modification to the outliner and journal GUIs to hide custom objectives during gameplay (Credit to Taylor)
7) Several "superevent" windows for extra flavor (Credit to Bananaman & Klein for the Newspaper window)
8) Modification to journal.gui to allow players to show a character icon in a journal entry (Credit to Mori)

Usage Notes:
* The Objective header can be hidden by setting the global variable community_gui_objective_var
* "Superevent" windows activated by including in event: gui_window = (event_window_crisis/event_window_newspaper/event_window_fullscreen)

## Parties ##
### Should we include parties at all? ###
Just Agrarian party included now as example. Use your mod detection triggers

## Community Mod Triggers ##

Usage
1) Place the file 00_community_mod_compatibility_triggers.txt  in the /common/scripted_triggers folder of your mod. This file will contain the scripted triggers all set to return false by default. This is intentional.
YOURMODNAME_is_active_trigger = {
  always = no
}

2) Create another file with the name zz_YOURMODNAME_compatibility_triggers.txt that contains the following:
YOURMODNAME_is_active_trigger = {
  always = yes
}

Currently Included:
* Anno 1836
* Australia & New Zealand Flavor Pack
* Basileia Romaion
* Better Decrees
* Better Politics Mod
* Community Outfit Mod
* East Asian Clothes Patch
* Gas, Guns, Garb, & Grub
* Gilded Age
* Greece, Byzantium, & the Balkans Flavor
* Grey's Little Reworks
* Hail, Columbia!
* James's Korea Flavor Pack
* James's Pop Clothing Tweaks
* Morgenrote: Dawn of Flavor
* Newspapers Mod
* Rally Round the King
* States That Make Sense
* Western Clothes: Redux
