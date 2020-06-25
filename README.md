# Installation
* Disable Trap Chests - Disables all encounters resulting from chests
* Force Trap Chests - Every chest will result in an encounter

See this tutorial on installing P4G mods for the smoothest experience: https://gamebanana.com/tuts/13379

# Development Notes
Used [Atlus Script Tools](https://github.com/TGEnigma/Atlus-Script-Tools) to decompile and recompile `dungeon.bf`.
It seems like there's a bug with those scripts that prevents recompiling of that script.
In particular, a variable `localVariable9` is not defined anywhere, but is reference repeatedly in the generated flowscript.
I resolved this by defining a `variable9`, but it could be that it should be referring to the global variable 9. Not sure... More testing required here, I might need to look into fixing Atlus Script Tools (or perhaps I'm misusing them somehow).