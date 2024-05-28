# Cat-Hub-Ui-library
you is finishing?

# Cat Hub Ui Library Loadstring
```-- Import Cat Hub UI library
local CatHubUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/1ForeverHD/CatHub/main/Main.lua"))()```

```-- Create a new window
local window = CatHubUI.CreateWindow("My Custom Script", UDim2.new(0, 300, 0, 200))```

-- Create a tab
local tab = window.CreateTab("Settings")
-- Create section for Walkspeed
local walkspeedSection = tab.CreateSection("Walkspeed Settings")

-- Create a slider for walkspeed
local walkspeedSlider = walkspeedSection.CreateSlider("Walkspeed", {min = 16, max = 100, default = 16}, function(value)
    game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = value
end)

-- Create toggle for walkspeed
local walkspeedToggle = walkspeedSection.CreateToggle("Toggle Walkspeed", function(enabled)
    if enabled then
        walkspeedSlider.SetEnabled(true)
    else
        walkspeedSlider.SetEnabled(false)
        game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = 16 -- Reset walkspeed
    end
end)

-- Create section for Movement
local movementSection = tab.CreateSection("Movement")

-- Create buttons for movement
local forwardButton = movementSection.CreateButton("Forward", function()
    -- Code for moving forward
end)

local backwardButton = movementSection.CreateButton("Backward", function()
    -- Code for moving backward
end)

local leftButton = movementSection.CreateButton("Left", function()
    -- Code for moving left
end)

local rightButton = movementSection.CreateButton("Right", function()
    -- Code for moving right
end)

-- Boot the UI library
CatHubUI.Boot()
