local Library = loadstring(game:HttpGet(""))()


-- Get Icon
-- For get icons, see lib/Icons.lua
Library:GetIcon("Home")

-- Set Theme
Library:SetTheme("Purple") -- See lib/Themes.lua

-- Set Window's Scale
Library:SetScale(1)


local Window = Library:MakeWindow({
    Title = "redz Library V5",
    SubTitle = "by : redz9999",
    SaveFolder = false -- Save Configs on Player's Device
})




-- Close Window (with user confirmation)
Window:CloseBtn()
-- Minimize Window (with user confirmation)
Window:MinimizeBtn()

-- Minimize Window
Window:Minimize()

-- Set New Title and/or Subtitle
Window:Set("New Title", "New Subtitle")

-- Select Tab
Window:SelectTab("Tab Name")


local Tab = Window:MakeTab({
    Title = "Tab",
    Icon = "Home" -- See lib/Icons.lua
})


local Section = Tab:AddSection({
    Title = "Section"
})

local Paragraph = Tab:AddParagraph({
    Title = "Paragraph",
    Text = "This is a Paragraph"
})


local Button = Tab:AddButton({
    Title = "Button",
    Desc = "Button's Description", -- Optional
    Callback = function ()
        print("Button Clicked")
    end
})


local Toggle = Tab:AddToggle({
    Title = "Toggle",
    Desc = "Toggle's Description", -- Optional
    Callback = function (Value)
        print("Toggle State Change", Value)
    end,
    Default = false, -- Default State
    Flag = false
})

