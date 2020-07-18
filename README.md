## Introduction ##
This include is created for [San Andreas Multiplayer](www.samp.com) Community, this include detects a player who uses Teleport hacks, you can do what ever you want underneath OnPlayerTeleport callback, OnPlayerTeleport is called when the include detects a player who is using Teleport hacks.

## Requeriments ##
* [Foreach](https://github.com/karimcambridge/samp-foreach/releases)

## Credits ##
* [PatrickGRT](https://github.com/PatrickGTR): Original code creator
* [Walter-Correa](https://github.com/Walter-Correa): Improvments and fixes
* [Pottus](https://github.com/Pottus): GetVehicleSpeed
* [karimcambridge](https://github.com/karimcambridge): Foreach

## Callback ##
    public OnPlayerTeleport(playerid, Float:distance, Float:oldx, Float:oldy, Float:oldz)
    {
	    if(IsPlayerInAnyVehicle(playerid) && GetPlayerState(playerid) == PLAYER_STATE_DRIVER) SetVehiclePos(GetPlayerVehicleID(playerid), oldx, oldy, oldz);
	    else SetPlayerPos(playerid, oldx, oldy, oldz);
	    return 1;
    }
