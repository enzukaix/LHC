# LuaHook Anti-Cheat

**Luahook Anti-Cheat (LHC) is a Roblox Anti-Cheat designed to stop cheaters before they even start exploiting. Unlike traditional Anti-Cheats in Roblox that usually detect the actual player behaviour (eg. Flying, Speedhacks) LHC works by checking the actual client behaviour and detecting additional tools that are used by the exploits, hooks, modifying the games attributes and players values.**

## Detections
Currently, LHC detects
- Namecall hooks/metatable tampering > (reliable)
- Exploit specific functions > (unreliable/Does not consistently detect)
```lua
exploitdtcs = {
	"getgenv",
	"hookfunction",
	"hookmetamethod",
	"getrawmetatable",
	"setreadonly",
	"islclosure",
	"checkcaller",
	"getnamecallmethod",
	"setnamecallmethod",
	"newcclosure",
	"getconnections",
	"getloadedmodules",
	"getsenv",
	"getreg",
	"getgc",
	"debug_getupvalues",
	"identifyexecutor",
	"getexecutorname",
	"request",
	"syn",
	"fluxus",
	"clonereference",
	"cloneref",
	"getcallingscript",
	"replicatesignal",
	"getscriptbytecode",
	"firesignal",
	"gethui",
	"protect_gui",
	"protectgui",
}
```
- Player Tampering > (reliable, eg. Fly, Walkspeed, jumpower, infinite jump, attribute tampering, Teleport, Tween, Velocity override)
- Logservice > (reliable) 
- GUI > (Roblox doesnt allow CoreGUI to be accessed so only unprotected GUIs can be flagged, Reliable) 
  ## Blacklisted User Handling
  **Blacklisted users are handled in multiple ways that the developer chooses by:**
  - Instant Bans
  - Kicks
  - Shadow Bans (Upon flagging a client, the server does not issue an immediate ban; instead, it enforces a designated delay period. This method significantly complicates the development and usage of exploits)
  - Freeze Client
  ## Developers and usage
** The developers can get LHC for free by reaching out to our discord server. Requirements:**
- Universal LHC (Obfuscated): 10.000+ Visits, 500+ CCU
- Game-Specific LHC (Obfuscated, we must have access to a game mechanics copy): 50.000+, 2500+ CCU
- Custom-Modified LHC (Unobfuscated): 1M+ Visits, 10.000+ CCU


