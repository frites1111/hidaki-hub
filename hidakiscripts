local mapScripts = {
    ["mugen"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Mugen_Train",
    ["ouwighara"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Dungeon",
    ["map2priv"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Map_2_PS",
    ["map1private"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Map_1_PS",
    ["map1public"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Map_1_PC",
    ["map2public"] = "https://raw.githubusercontent.com/frites1111/hidaki-hub/main/Map_2_PC"
}

-- Function to detect the current map
local function getCurrentMap()
    for _, v in pairs(game.Workspace:GetChildren()) do
        if mapScripts[v.Name] then
            return v.Name
        end
    end
    return nil
end

-- Load the correct script
local currentMap = getCurrentMap()
if currentMap and mapScripts[currentMap] then
    loadstring(game:HttpGet(mapScripts[currentMap]))() -- ✅ This will now work correctly
else
    warn("No script found for this map!")
end
