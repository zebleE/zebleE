local plr = game.Players.LocalPlayer
local MainScript = game:FindFirstChild("Rerubi" , true).Parent.Parent
local ScreenGui = Instance.new("ScreenGui" , plr.PlayerGui)
local MainFrame = Instance.new("Frame" , ScreenGui)
local ScrollingFrame = Instance.new("ScrollingFrame" , MainFrame)
local TextBox = Instance.new("TextBox" , ScrollingFrame)
local Logo1 = Instance.new("TextLabel" , MainFrame)
local Logo2 = Instance.new("TextLabel" , MainFrame)
local Logo3 = Instance.new("TextLabel" , MainFrame)
local Dec1 = Instance.new("Frame" , MainFrame)
local Dec2 = Instance.new("Frame" , MainFrame)
local UIGradient1 = Instance.new("UIGradient" , Dec1)
local UIGradient2 = Instance.new("UIGradient" , Dec2)
local ClearButton = Instance.new("TextButton" , MainFrame)
local ExecuteButton = Instance.new("TextButton" , MainFrame)
local ProfileImage = Instance.new("ImageLabel" , MainFrame)
local UICorner1 = Instance.new("UICorner" , MainFrame)
local UICorner2 = Instance.new("UICorner" , ExecuteButton)
local UICorner3 = Instance.new("UICorner" , ClearButton)


MainFrame.Position = UDim2.new(0.193, 0,0.221, 0)
MainFrame.Size = UDim2.new(0.631, 0,0.572, 0)
MainFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
UICorner1.CornerRadius = UDim.new(0 , 8)
UICorner2.CornerRadius = UDim.new(0 , 8)
UICorner3.CornerRadius = UDim.new(0 , 8)
ScrollingFrame.Position = UDim2.new(0.018, 0,0.145, 0)
ScrollingFrame.Size = UDim2.new(0.963, 0,0.692, 0)
ScrollingFrame.ScrollBarImageColor3 = Color3.fromRGB(86, 86, 86)
ScrollingFrame.ScrollBarThickness = 12
ScrollingFrame.CanvasSize = UDim2.new(0, 0,1.6, 0)
ScrollingFrame.Transparency = 1
TextBox.Position = UDim2.new(0 , 0 , 0 , 0)
TextBox.Size = UDim2.new(0, 562,0, 564)
TextBox.BackgroundColor3 = Color3.new(0, 0, 0)
TextBox.TextSize = 10
TextBox.Text = ""
TextBox.PlaceholderText = "script here..."
TextBox.TextColor3 = Color3.new(1, 1, 1)
TextBox.TextXAlignment = Enum.TextXAlignment.Left
TextBox.TextYAlignment = Enum.TextYAlignment.Top
ExecuteButton.Position = UDim2.new(0.76, 0,0.894, 0)
ExecuteButton.Size = UDim2.new(0.222, 0,0.076, 0)
ExecuteButton.BackgroundColor3 = Color3.fromRGB(44, 44, 44)
ExecuteButton.TextColor3 = Color3.new(1, 1, 1)
ExecuteButton.TextScaled = true
ExecuteButton.Text = "Run"
ClearButton.Position = UDim2.new(0.499, 0,0.894, 0)
ClearButton.Size = UDim2.new(0.222, 0,0.076, 0)
ClearButton.BackgroundColor3 = Color3.fromRGB(44, 44, 44)
ClearButton.TextColor3 = Color3.new(1, 1, 1)
ClearButton.TextScaled = true
ClearButton.Text = "Clear"
Dec1.Position = UDim2.new(-0.001, 0,0.867, 0)
Dec2.Position = UDim2.new(0.001, 0,0.117, 0)
Dec1.BorderSizePixel = 0
Dec2.BorderSizePixel = 0
Dec1.Size = UDim2.new(1, 0,-0.005, 0)
Dec2.Size = UDim2.new(1, 0,-0.005, 0)
UIGradient1.Color = ColorSequence.new(Color3.new(0, 0.0156863, 1) , Color3.new(0.435294, 1, 0.886275))
UIGradient2.Color = ColorSequence.new(Color3.new(1, 0.235294, 0) , Color3.new(0.866667, 1, 0))
Logo1.Position = UDim2.new(0.295, 0,0.174, 0)
Logo1.Size = UDim2.new(0.409, 0,0.65, 0)
Logo1.BackgroundTransparency = 1
Logo1.TextScaled = true
Logo1.Text = "R"
Logo1.TextTransparency = .5
Logo1.TextColor3 = Color3.fromRGB(108, 108, 108)
Logo1.FontFace.Style = Enum.FontStyle.Italic
Logo1.Font = Enum.Font.TitilliumWeb
Logo2.Position = UDim2.new(0.018, 0,-.01, 0)
Logo2.Size = UDim2.new(0.164, 0,0.123, 0)
Logo2.BackgroundTransparency = 1
Logo2.Text = "Root"
Logo2.TextColor3 = Color3.new(1, 1, 1)
Logo2.Font = Enum.Font.TitilliumWeb
Logo2.TextScaled = true
Logo3.Position = UDim2.new(0.145, 0,0, 0)
Logo3.Size = UDim2.new(0.154, 0,0.057, 0)
Logo3.BackgroundTransparency = 1
Logo3.Text = "serverSide"
Logo3.TextColor3 = Color3.new(1, 1, 1)
Logo3.Font = Enum.Font.Jura
Logo3.TextScaled = true
ProfileImage.Position = UDim2.new(0.935, 0,0.019, 0)
ProfileImage.Size = UDim2.new(0.047, 0,0.082, 0)
ProfileImage.Image = "http://www.roblox.com/Thumbs/Avatar.ashx?x=100&y=100&username="..tostring(plr)


ExecuteButton.MouseButton1Down:Connect(function()
	MainScript.RemoteEvent:FireServer(TextBox.Text)
end)
ClearButton.MouseButton1Down:Connect(function()
	TextBox.Text = ""
end)
