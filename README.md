local Library = {}

function Library.CreateMain()
	local ScreenGui = Instance.new("ScreenGui")
	local Frame = Instance.new("Frame")
	local UIListLayout = Instance.new("UIListLayout")
	
	ScreenGui.Parent = game.CoreGui

	Frame.Parent = ScreenGui
	Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Frame.Position = UDim2.new(0.33764258, 0, 0.249554425, 0)
	Frame.Size = UDim2.new(0, 400, 0, 302)
	
	UIListLayout.Parent = Frame
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.VerticalAlignment = Enum.VerticalAlignment.Center
	
	local GamerLibrary = {}
	
	function GamerLibrary:Button(name, callback)
		
		local TextBox = Instance.new("TextBox")
		
		TextBox.Name = name
		TextBox.Text = name
		TextBox.Parent = Frame
		TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.Position = UDim2.new(0.25, 0, 0.357615888, 0)
		TextBox.Size = UDim2.new(0, 200, 0, 50)
		TextBox.Font = Enum.Font.SourceSans
		TextBox.Text = "Textbox"
		TextBox.TextColor3 = Color3.fromRGB(0, 0, 0)
		TextBox.TextSize = 14.000
		
		Frame:FindFirstChild(name).MouseButton1Click:connect(callback)
	end
	
	return GamerLibrary
	
end

return Library
