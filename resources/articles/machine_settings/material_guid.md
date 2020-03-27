Material GUID
====
This setting contains a unique identifier for the material that's on the spool currently loaded in the printer. This uniquely identifies the plastic that gets fed into the printer, including its manufacturer and colour. It will be the same between different spools of the same material though. Basically, each different item you'd see in an online shop would get a unique identifier. Cura uses this unique identifier for two purposes: to sync the configuration with whatever is on your printer (if your printer is connected to Cura) and to group profiles together that belong to the same material.

When an Ultimaker printer is connected to Cura over the network or the internet, the printer provides Cura with a list of GUIDs for the materials that are currently loaded into the printer. Cura matches these GUIDs with the GUIDs in its profiles, by which it knows which profiles to display to the user.

It's also used to group the available quality levels for a certain material. Cura's profile system is very complex, and this is one of its quirks: Normally Cura will display all quality profiles available for the current material type. That is to say, if a certain manufacturer indicates that his material is a type of PLA, all quality profiles for PLA will be available. However when there is any quality profile that specifies the current material by GUID, then only that quality profile will be available. This essentially means that there are profiles specifically tailored for this filament, and the generic profiles should no longer be shown.