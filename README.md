# [TF2] Generic Menu

This plugin is meant for simple way to create sourcemod menus. I struggled to find a way myself, now that i know a bit i want to show others how to do it.

This is a plugin that i created ~~(Mostly CopilotAI)~~. Because i needed a custom menu for giving custom weapons easily (instead of having to type the command each time).
This is my 2nd plugin ever created (1st one already existed) ~~so any suggestions, helping is appreciated~~ (I have almost 0 coding experience (Enough for this i guess))

Basic Installition (For fast install and no editing code)
- Put .smx into sourcemod/plugins.
- ~~(Optional)Put .cfg into sourcemod/configs.~~ Automaticly creates config.
- Load plugin or restart the server.

Config file automaticly gets created at addons/sourcemod/configs/menu_items.cfg
This plugin uses sourcemod chat triggers so whatever your config is, thats what it will use.
It only recognizes %n as Username and %u as UserID (for config file only)

Advanced Installition (To change menu name, config name and to change config location/creation (usefull for more than 1 menu with more than 1 plugin of this)
- Edit the .sp file with desired names/definitions (Mosty defined at top)
- Put the .sp file in `sourcemod/scripting`
- Run the compile.exe with cmd (open cmd, go to the location of compile.exe) with the plugin name (example: compile GenericMenu.sp
- Put the .smx file thats created in `sourcemod/scripting/compiled` to `sourcemod/plugins`
- Load the plugin (sm plgugins load GenericMenu.smx)/ map change or restart the server

Base plugin (attached .smx and .sp file) is only for ROOT admins, you can change required admin level (if its on admin only mode) in the sp file on top (somewhere in #define parts)

Commands: (Affected by SourceMod triggers)
- `sm_menu` (Opens the menu)
- `sm_reloadmenu` (Reloads the config)

ConVar(s): (sm_cvar command or from server console)
- `sm_genericmenu_enabled` "1" (1 = enabled, else = disabled)
- `sm_genericmenu_debug` "0" (1 = enabled, else = disabled)
- `sm_genericmenu_admin_require` "1" (1 = enabled, else = disabled)

I had a lot of inspiration from theY4Kman's Triggers plugin. https://forums.alliedmods.net/showthread.php?p=585758
