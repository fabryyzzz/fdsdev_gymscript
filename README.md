# Setting up PERK effects 

```lua
RegisterNetEvent("fdsdev_gymscript:recieveData", function()
    
end)
```

In _**config.lua**_ you can find this event. This event is triggered when a perk's level XP is updated. You can use this to configure perk actions.
Example: 
```lua
RegisterNetEvent("fdsdev_gymscript:recieveData", function()
    if GetLivelloPerk("terzoperk") > 1 then
        -- action
    end
end)
```

# PERK IDs

* First perk: "**forza**"
* Second perk: "**resistenza**"
* Third perk: "**terzoperk**"
# Exports

## GetLivelloPerk
```lua
local perkid = "forza"
exports.fdsdev_gymscript:GetLivelloPerk(perkid)
```
## getEsercizio
```lua
exports.fdsdev_gymscript:getEsercizio()
```
This export will return the current exercise.
## GetPeso
```lua
local type = "forza"
exports.fdsdev_gymscript:GetPeso(type)
```
This export will return the weight corresponding to the perk level you are at. 
Works only with theese types:
* panca
* spalle
* bicipiti
## OpenStats
```lua
exports.fdsdev_gymscript:OpenStats()
```
This export will open the stats interface.
