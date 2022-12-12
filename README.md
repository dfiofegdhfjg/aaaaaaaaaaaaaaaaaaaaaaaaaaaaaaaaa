local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Rayfield/main/source'))()
local Window = Rayfield:CreateWindow({
	Name = "Lucifer Hub",
	LoadingTitle = "Lucifer Hub",
	LoadingSubtitle = "...",
	ConfigurationSaving = {
		Enabled = true,
		FolderName = nil, -- Create a custom folder for your hub/game
		FileName = "Big Hub"
	},
        Discord = {
        	Enabled = false,
        	Invite = "sirius", -- The Discord invite code, do not include discord.gg/
        	RememberJoins = true -- Set this to false to make them join the discord every time they load it up
        },
	KeySystem = true, -- Set this to true to use our key system
	KeySettings = {
		Title = "Lucifer Hub",
		Subtitle = "Key System",
		Note = "The Key Is 1234",
		FileName = "SiriusKey",
		SaveKey = true,
		GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
		Key = "1234"
	}
})

--Tabs
local MainTab = Window:CreateTab("Main", 4483362458) -- Title, Image
local MainSection = Tab:CreateSection("Main Section")

local Toggle = Tab:CreateToggle({
	Name = "Speed!",
	CurrentValue = false,
	Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 120
    	
})

local Button = Tab:CreateButton({
	Name = "GodMode!",
	Callback = function()
		game.Players.LocalPlayer.Character.Humanoid.MaxHealth = 10000000
        game.Players.LocalPlayer.Character.Humanoid.Health = 10000000
	end,
})
