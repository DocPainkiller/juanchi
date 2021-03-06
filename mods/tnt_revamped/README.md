# tnt
Fork of [TNT](https://github.com/minetest/minetest_game/tree/master/mods/tnt) mod

water flow code copied from TenPlus1's builtin_item mod [builtin_item](https://notabug.org/TenPlus1/builtin_item)

# Features 

1. TNT is always entity on ignite.

2. TNT entitys flow in water.

3. TNT jumps on ignite.

4. It is possible to make minecraft style TNT cannons with this mod.

5. TNT does not damage nodes if in water.

# api

``` lua
tnt.register_tnt({
    -- Mod name : TNT name
    name = "tnt:tnt",
    -- Description of TNT node
    description = "TNT",
    -- TNT Blast radius.
    radius = tnt_radius,
    -- Strength of blast (explosions mod only).
    strength = 1000,
    -- explosion delay in seconds.
    time = 4,
    -- On ignite the TNT will jump upwards based on the jump value.
    jump = 3,
    -- Ignite sound effect.
    ignite_sound = {name = "tnt_ignite"},
    -- The explosion sound effect.
    boom_sound = {name = "tnt_explode", def = {gain = 1.5, max_hear_distance = 128}}
})
```

# Config

The size of the default tnt blast.

``` lua
tnt_radius = 3
```

The number to multiply the TNT's entity knockback velocity on blast.

``` lua
tnt_revamped.entity_velocity_mul = 2
```

The explosion api to use.

Use the default tnt explosion api from the TNT mod.

Use the explosions api from ryvnf's explosions mod.

``` lua
tnt_revamped.explosion = "default"
```

**In Water**

If true TNT blast will be able to damage nodes even if its in water.

``` lua
tnt_revamped.damage_nodes = false
```

If true TNT blast will be able to damage entities even if its in water.

``` lua
tnt_revamped.damage_entities = false
```

Authors of source code
----------------------
PilzAdam (MIT)

ShadowNinja (MIT)

sofar (sofar@foo-projects.org) (MIT)

Various Minetest developers and contributors (MIT)
