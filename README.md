Private browsing
================

Private browsing tabs for the Luakit browser.

Install by copying the private_browsing_tabs.lua file into ~/.config/luakit/plugins/
and by adding
```
require "plugins.private_browsing_tab" 
```
to your rc.lua in ~/.config/luakit/

Add a command to the add_cmds call in your binds.lua to toggle private browsing on and off.

For example:
```lua
add_cmds({
    ...
    cmd("pr[ivate]", "Toggle private browsing",                                             function (w)                                                                 
             w.view.enable_private_browsing = not w.view.enable_private_browsing
             w:update_tablist()
       end),
    ...
})
```
This allows you to use commands :pr and :private to toggle private browsing on and off.
