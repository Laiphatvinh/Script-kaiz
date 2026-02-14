local correctKey = "VINH2026"

local gui = Instance.new("ScreenGui", game.Players.LocalPlayer.PlayerGui)

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0,300,0,180)
frame.Position = UDim2.new(0.5,-150,0.5,-90)
frame.BackgroundColor3 = Color3.fromRGB(35,35,35)

local box = Instance.new("TextBox", frame)
box.Size = UDim2.new(0.8,0,0,40)
box.Position = UDim2.new(0.1,0,0.3,0)
box.PlaceholderText = "Nhập key..."

local button = Instance.new("TextButton", frame)
button.Size = UDim2.new(0.8,0,0,40)
button.Position = UDim2.new(0.1,0,0.6,0)
button.Text = "Xác nhận"

button.MouseButton1Click:Connect(function()
    if box.Text == correctKey then
        print("Key đúng — mở menu")
        frame:Destroy()
        -- loadstring(game:HttpGet("https://raw.githubusercontent.com/HieuDepTrai-Z/Dev_Orange/refs/heads/main/OrangeHub.lua"))()
        
    else
        box.Text = ""
        box.PlaceholderText = "Sai key!"
    end
end)
