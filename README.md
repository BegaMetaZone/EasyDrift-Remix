# This is a Redesign 
So all the functionality is still there and unchanged except some UI elements . 
I included 5 badges that change based on the drift score bracket , honestly I might redesign the second one or add few more .
Make sure to name the resource "EasyDrift" not "EasyDrift-Remix-Main" or "EasyDrift-Main"

# EasyDrift
## A simple drift counter

EasyDrift is a simple drift counter that also provides a multitude of events and functions to integrate the system with your own HUD

- Drag and drop if you don't want to loose time !
- Fixed a popular issue on drift counter where low fps would get less score
- Easy integration with your own HUD
- Pre made HUD *inspired* by forza

![image](https://forum.cfx.re/uploads/default/original/4X/6/c/b/6cb0eb024218c8da4651c58485e3ade01072cef3.png)


## Events (Client side)

EasyDrift provides a list of events to use to integrate the system with your framework or HUD. Want to give money as a reward to your players after a great drift? It's possible!
Each event name can be changed in the resource's config file.


| Event | Default event name | Argument passed |
| ------ | ------ | ------ |
| Start drifting | drift:start | none |
| Stop drifting | drift:finish | 1: final score |
| Enable counter | drift:enable | none |
| Disable counter | drift:disable | none |
| Toggle counter | drift:toggle | none |


Some events are also available to retrieve information

`drift:GetCurrentDriftScore`
Get the current drift score
```
-- Exemple usage
TriggerEvent("drift:GetCurrentDriftScore", function(score)
    print("My score is: ", score) 
end)
```

`drift:IsDrifting`
Get if the player is drifting or not
```
-- Exemple usage
TriggerEvent("drift:IsDrifting", function(isDrifting)
    print("Am i drifitng ? ", isDrifting) 
end)
```

`drift:IsEnabled`
Check counter is enabled
```
-- Exemple usage
TriggerEvent("drift:IsEnabled", function(isEnabled)
    print("Is the counter enabled ? ", isEnabled) 
end)
```


# Advanced developer

A global export is also available allowing you to access all the variables / functions of the code from another resource. I don't recommend to use this if you are not sure of what you are doing.
Export name `GetModules`
```
-- Exemple usage
local Modules = exports[‘EasyDrift’]:GetModules()
print(Modules.DriftCounter.CurrentPoints)
```


# Support

Want some support or request something to be added ? Come here !

[![Discord2](https://discordapp.com/api/guilds/926120299232112671/widget.png?style=banner4)](https://discord.gg/fhgc3s8HzS)

