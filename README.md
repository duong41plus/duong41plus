local ScreenGui = Instance.new("ScreenGui")
local DUPEFRAME = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local DUPENAME = Instance.new("TextLabel")
local DUPEBUTTON = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local UNDOBUTTON = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local statusdupe = Instance.new("TextLabel")
local STATUSSTART = Instance.new("TextLabel")
local rejoinbutton = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local STATUSSTOPLOSS = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

DUPEFRAME.Name = "DUPEFRAME"
DUPEFRAME.Parent = ScreenGui
DUPEFRAME.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
DUPEFRAME.BorderColor3 = Color3.fromRGB(0, 0, 0)
DUPEFRAME.BorderSizePixel = 0
DUPEFRAME.Position = UDim2.new(0.401397049, 0, 0.414117634, 0)
DUPEFRAME.Size = UDim2.new(0, 314, 0, 156)
DUPEFRAME.Active = true
DUPEFRAME.Visible = true
DUPEFRAME.Draggable = true

UICorner.CornerRadius = UDim.new(0.300000012, 0)
UICorner.Parent = DUPEFRAME

DUPENAME.Name = "DUPENAME"
DUPENAME.Parent = DUPEFRAME
DUPENAME.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
DUPENAME.BorderColor3 = Color3.fromRGB(0, 0, 0)
DUPENAME.BorderSizePixel = 0
DUPENAME.Position = UDim2.new(0.181528658, 0, 0, 0)
DUPENAME.Size = UDim2.new(0, 200, 0, 50)
DUPENAME.Font = Enum.Font.SourceSans
DUPENAME.Text = "DUONG CODER"
DUPENAME.TextColor3 = Color3.fromRGB(255, 255, 255)
DUPENAME.TextSize = 54.000

DUPEBUTTON.Name = "DUPEBUTTON"
DUPEBUTTON.Parent = DUPEFRAME
DUPEBUTTON.BackgroundColor3 = Color3.fromRGB(85, 255, 127)
DUPEBUTTON.BorderColor3 = Color3.fromRGB(0, 0, 0)
DUPEBUTTON.BorderSizePixel = 0
DUPEBUTTON.Position = UDim2.new(0.0700636953, 0, 0.487179488, 0)
DUPEBUTTON.Size = UDim2.new(0, 120, 0, 50)
DUPEBUTTON.Font = Enum.Font.SourceSans
DUPEBUTTON.Text = "START"
DUPEBUTTON.TextColor3 = Color3.fromRGB(0, 0, 0)
DUPEBUTTON.TextSize = 35.000
DUPEBUTTON.MouseButton1Down:Connect(function()
        game:GetService("ReplicatedStorage").Remote.SetDungeonSetting:FireServer("Theme",  Options[Options.Current])
	STATUSSTART.Visible = true
	STATUSSTART.Active = true
	STATUSSTOPLOSS.Visible = false
	STATUSSTOPLOSS.Active = false
end)

UICorner_2.CornerRadius = UDim.new(0.300000012, 0)
UICorner_2.Parent = DUPEBUTTON

UNDOBUTTON.Name = "UNDOBUTTON"
UNDOBUTTON.Parent = DUPEFRAME
UNDOBUTTON.BackgroundColor3 = Color3.fromRGB(255, 21, 0)
UNDOBUTTON.BorderColor3 = Color3.fromRGB(0, 0, 0)
UNDOBUTTON.BorderSizePixel = 0
UNDOBUTTON.Position = UDim2.new(0.557324827, 0, 0.487179488, 0)
UNDOBUTTON.Size = UDim2.new(0, 120, 0, 50)
UNDOBUTTON.Font = Enum.Font.SourceSans
UNDOBUTTON.Text = "STOP"
UNDOBUTTON.TextColor3 = Color3.fromRGB(0, 0, 0)
UNDOBUTTON.TextSize = 35.000
UNDOBUTTON.MouseButton1Down:Connect(function()
        game:GetService("ReplicatedStorage").Remote.SetDungeonSetting:FireServer("Theme", Options.Undo)
	STATUSSTART.Visible = false
	STATUSSTART.Active = false
	STATUSSTOPLOSS.Visible = true
	STATUSSTOPLOSS.Active = true
end)

UICorner_3.CornerRadius = UDim.new(0.300000012, 0)
UICorner_3.Parent = UNDOBUTTON

statusdupe.Name = "statusdupe"
statusdupe.Parent = DUPEFRAME
statusdupe.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
statusdupe.BorderColor3 = Color3.fromRGB(0, 0, 0)
statusdupe.BorderSizePixel = 0
statusdupe.Position = UDim2.new(0, 0, 0.319186479, 0)
statusdupe.Size = UDim2.new(0, 86, 0, 27)
statusdupe.Font = Enum.Font.SourceSans
statusdupe.Text = "status :"
statusdupe.TextColor3 = Color3.fromRGB(255, 255, 255)
statusdupe.TextSize = 30.000

STATUSSTART.Name = "STATUSSTART"
STATUSSTART.Parent = DUPEFRAME
STATUSSTART.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
STATUSSTART.BorderColor3 = Color3.fromRGB(0, 0, 0)
STATUSSTART.BorderSizePixel = 0
STATUSSTART.Position = UDim2.new(0.315286636, 0, 0.340362549, 0)
STATUSSTART.Size = UDim2.new(0, 89, 0, 19)
STATUSSTART.Font = Enum.Font.SourceSans
STATUSSTART.Text = "dupe started"
STATUSSTART.TextColor3 = Color3.fromRGB(255, 255, 255)
STATUSSTART.TextSize = 28.000
STATUSSTART.Visible = false
STATUSSTART.Active = false

rejoinbutton.Name = "rejoinbutton"
rejoinbutton.Parent = DUPEFRAME
rejoinbutton.BackgroundColor3 = Color3.fromRGB(255, 170, 255)
rejoinbutton.BorderColor3 = Color3.fromRGB(0, 0, 0)
rejoinbutton.BorderSizePixel = 0
rejoinbutton.Position = UDim2.new(0.181528658, 0, 0.846153855, 0)
rejoinbutton.Size = UDim2.new(0, 200, 0, 18)
rejoinbutton.Font = Enum.Font.SourceSans
rejoinbutton.Text = "REJOIN"
rejoinbutton.TextColor3 = Color3.fromRGB(0, 0, 0)
rejoinbutton.TextSize = 20.000
rejoinbutton.MouseButton1Down:Connect(function()
local ts = game:GetService("TeleportService")

local p = game:GetService("Players").LocalPlayer



ts:TeleportToPlaceInstance(game.PlaceId, game.JobId, p)
end)

UICorner_4.CornerRadius = UDim.new(0.600000024, 0)
UICorner_4.Parent = rejoinbutton

STATUSSTOPLOSS.Name = "STATUSSTOPLOSS"
STATUSSTOPLOSS.Parent = DUPEFRAME
STATUSSTOPLOSS.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
STATUSSTOPLOSS.BorderColor3 = Color3.fromRGB(0, 0, 0)
STATUSSTOPLOSS.BorderSizePixel = 0
STATUSSTOPLOSS.Position = UDim2.new(0.273885339, 0, 0.339743584, 0)
STATUSSTOPLOSS.Size = UDim2.new(0, 122, 0, 19)
STATUSSTOPLOSS.Font = Enum.Font.SourceSans
STATUSSTOPLOSS.Text = "dupe stopped"
STATUSSTOPLOSS.TextColor3 = Color3.fromRGB(255, 255, 255)
STATUSSTOPLOSS.TextSize = 28.000
STATUSSTOPLOSS.Visible = false
STATUSSTOPLOSS.Active = false
