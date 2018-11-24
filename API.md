#Grenades API

Still WIP. Please suggest new features here: https://forum.minetest.net/viewtopic.php?f=9&t=21466

##API

	`grenades.register_grenade("name", { -- Name of the grenade (Like 'smoke' or 'flashbang')
		description = "", -- A short description of the grenade.
		image = "", -- The name of the grenade's texture
		on_explode = function(pos, name)
			-- This function is called when the grenade 'explodes'
			-- <pos> the place the grenade 'exploded' at
			-- <name> the name of the player that threw the grenade
		end,
		placeable = false, -- Optional, default is false
		timeout = 5, -- Optional, default is 5
		particle = { -- Adds particles in the grenade's trail
            image = "grenades_smoke.png", -- The particle's image
            life = 1, -- How long (seconds) it takes for the particle to disappear
            size = 4, -- Size of the particle
            glow = 0, -- brightens the texture in darkness
        }
	})`