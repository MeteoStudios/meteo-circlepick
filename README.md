# Meteo Circlepick Minigame
# Avaialbe at : https://meteofivem.net/fivem-scripts/prodigy-rp-inspired-circlepick-minigame

A circle-based lockpicking minigame script for FiveM.

## Features

- Dynamic difficulty system (Easy, Medium, Hard)
- Randomized time limits based on difficulty
- Success/failure notifications

## Installation

### QBCore Framework (qb-vehiclekeys)

**Pre-configured Version (Recommended)**
You can just download qb-vehiclekeys modified for support of meteo-circlepick - https://github.com/MeteoFivem/qb-vehiclekeys

**Manual**
- Go to `[qb]/qb-vehiclekeys/client/main.lua`
- Look for `RegisterNetEvent('lockpicks:UseLockpick')` event
- Find `local success = exports['qb-minigames']:Skillbar(difficulty)`
- Replace it with `local success = exports['meteo-circlepick']:startLockpick(difficulty, nil)`

### QBox Framework (qbx_vehiclekeys)

**Pre-configured Version (Recommended)**
You can just download qbx_vehiclekeys modified for support of meteo-circlepick - https://github.com/MeteoFivem/qbx_vehiclekeys

**Manual**
- Go to `[qbx]/qbx_vehiclekeys/client/functions.lua`
- Look for function `LockpickDoor`
- Find `local isSuccess = customChallenge or lib.skillCheck(skillCheckConfig.difficulty, skillCheckConfig.inputs)`
- Replace it with `local isSuccess = customChallenge or exports['meteo-circlepick']:startLockpick(difficulty, nil)`
- Again look for function `Hotwire`
- Find the skillCheck line
- Replace it with `local isSuccess = customChallenge or exports['meteo-circlepick']:startLockpick(skillCheckConfig.difficulty, nil)`

## For Developers

Export the lockpick function in your scripts:

```lua
local success = exports['meteo-circlepick']:startLockpick(difficulty, timeLimit)
```

### Parameters

- `difficulty`: String - "easy", "medium", or "hard"
- `timeLimit`: Number - Time limit in seconds

### Event Handler

```lua
TriggerEvent('meteo-circlepick:client:openLockpick', function(success)
    if success then
        -- Handle successful lockpick
    else
        -- Handle failed lockpick
    end
end)
```

## Note

This script is exclusively available through official Meteo Studios FiveM and we are only selling this script through Tebex and it comes to your FiveM CFX Account. Beware of unauthorized copies or scams from other sources.

*For technical support, bug reports, or questions, please use our Discord server. We're here to help!*

## Links

- **Script Link**: https://meteofivem.net/fivem-scripts/prodigy-rp-inspired-circlepick-minigame
- **Website**: https://meteofivem.net/

- **Discord**: https://discord.com/invite/wxp9gaVrqa
