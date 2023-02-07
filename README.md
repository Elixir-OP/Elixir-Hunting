# Elixir Hunting
OPEN SOURCE Available here: https://elixirfw.tebex.io/package/5515717

ESCROWED Available here: https://elixirfw.tebex.io/package/5515715

# Info
In our script we have created a version that will allow you to hunt animals, to pick up their meat, and then to sell them at a place in which you have the option of buying hunting weapons and ammo as well as using a hunting knife to cut down the animals and sell the meat. Is compatible with QB-target.

# Features
1. QBCore supported.
2. Custom QBCore rename supported in config.
3. Fully configurable.
4. Open-Source/Encrypted Both Available
5. When you enter or leave hunting zone, you get a notification and a sound.
6. There is no chance of being able to fire from hunting weapons outside the radius of a hunting zone set in configuration.

# How to install
### Rename Core
* Go to ``config.lua`` and search for this:
```
Config.Corename = 'qb-core'
```

### Choose target
* Go to ``config.lua`` and search for this:
```
Config.Target = 'qb-target' -- qb-target/bt-target Whatever You use
```

### Choose Hunting Weapon
* Go to ``config.lua`` and search for this:
```
Config.HuntWeapon = 'weapon_musket' -- Weapon will be set here so it can sync with not firing while outside hunting zone and with Shop.
```

### Choose Hunting Store Ped(Can be Found Here https://docs.fivem.net/docs/game-references/ped-models/)
* Go to ``config.lua`` and search for this:
```
Config.ShopPed = 'cs_hunter'  --- Model of The Shop Ped
```

### Choose Hunting Store Target Distance
* Go to ``config.lua`` and search for this:+
```
Config.ShopTargetDistance = 2.0 --- This is the Distance from how far the target can be used
```

### Configuration
* Go the ``config.lua`` file
* Configure Animals Meat Amount which you get after cutting them
```
Config.Animals = {
    [GetHashKey("a_c_mtlion")] = {
        meatAmount = {min = 3, max = 7},
        meatName = "lion_meat",
    },

    [GetHashKey("a_c_deer")] = {
        meatAmount = {min = 5, max = 10},
        meatName = "deer_meat",
    },

    [GetHashKey("a_c_pig")] = {
        meatAmount = {min = 4, max = 7},
        meatName = "pig_meat",
    },

    [GetHashKey("a_c_rabbit_01")] = {
        meatAmount = {min = 1, max = 2},
        meatName = "rabbit_meat",
    }
}
```

* Configure Meat Prices:
```
Config.Prices = {
    Items = {
        ["lion_meat"] = {min = 10, max = 10},
        ["deer_meat"] = {min = 8, max = 8},
        ["pig_meat"] = {min = 7, max = 7},
        ["rabbit_meat"] = {min = 6, max = 6},
    }
}
```

* Configure Locations:
```
Config.Locations = {
    ["shopLoc"] = vector3(-679.8206, 5838.873, 17.331434),
    ["shopPed"] = vector4(-679.72, 5839.01, 17.33, 226.23),
    ["huntZone"] = vector3(-1189.043, 4661.6391, 249.82835),
    ["huntZoneRadius"] = 450.00
}
```

* Configure Shop Items:
```
Config.Shop = {
    label = "Hunting Shop",
    slots = 20,
    items = {
        {
            name = Config.HuntWeapon,
            price = 2000,
            amount = 1,
            info = {},
            type = "weapon",
            slot = 1,
        },
        {
            name = "shotgun_ammo",
            price = 50,
            amount = 1,
            info = {},
            type = "item",
            slot = 2,
        },
        {
            name = "hunting_knife",
            price = 50,
            amount = 1,
            info = {},
            type = "item",
            slot = 3,
        },
    }
}
```

* Configure Notification Messages:
```
Config.NoDeadAnimal = ("You aren't close to any dead animal")
Config.EnterHunt = ("You entered the hunting zone, Good luck!")
Config.ExitHunt = ("You exited the hunting zone!")
```

### Items
* Add the Following to your items list in your core/base:
```
	-------------Hunting
	["deer_meat"]                   = {["name"] = "deer_meat",              ["label"] = "Deer Meat",           ["created"] = nil, 		["decay"] = 30.0,      ["weight"] = 1000,         ["type"] = "item",         ["image"] = "meat.png", ["unique"] = false,        ["useable"] = true,          ["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Boom boom we have meat to night"},
	["rabbit_meat"]                 = {["name"] = "rabbit_meat",          	["label"] = "Rabbit Meat",         ["created"] = nil, 		["decay"] = 30.0,       ["weight"] = 1000,         ["type"] = "item",         ["image"] = "meat.png", ["unique"] = false,        ["useable"] = true,          ["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Boom boom we have meat to night"},
	["lion_meat"]                   = {["name"] = "lion_meat",              ["label"] = "Lion Meat",           ["created"] = nil, 		["decay"] = 30.0,     ["weight"] = 1000,         ["type"] = "item",         ["image"] = "meat.png", ["unique"] = false,        ["useable"] = true,          ["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Boom boom we have meat to night"},
	["pig_meat"]                    = {["name"] = "pig_meat",               ["label"] = "Pig Meat",            ["created"] = nil, 		["decay"] = 30.0,    ["weight"] = 1000,         ["type"] = "item",         ["image"] = "meat.png", ["unique"] = false,        ["useable"] = true,          ["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Boom boom we have meat to night"},
	["hunting_knife"]               = {["name"] = "hunting_knife",          ["label"] = "Hunting Knife",       ["created"] = nil, 		["decay"] = 30.0,         ["weight"] = 1000,         ["type"] = "item",         ["image"] = "huntingknife.png", ["unique"] = false,        ["useable"] = true,          ["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Hunt for some meat"},
```
* Add these items to your qb-inventory > html > images, images found in images folder

![Meat PNG](https://media.discordapp.net/attachments/627417439566561290/1072591534823833620/meat.png) 
![Hunting Knife](https://media.discordapp.net/attachments/627417439566561290/1072592797443563550/huntingknife.png) 

### Hunting Store MLO (I Don't Promote Leaks It's just for the testing Purpose.)

### Support
For issues join our [Discord](https://discord.gg/JMTPdBV), and we will help you asap!
