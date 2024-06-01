su06042_80711 - Beta tester

Zephy | @helloworld26445 - 100% of work

https://discord.gg/8teQdSBGMb <--- Join for more updates

# Aurora Version 2

### Docs

## Creating a window
```lua
local Window = library:Window({
    title = "Name of the library"
})
--[[
title = <string> - The title displayed on the window.
]]
```

## Adding a tab
```lua
-- Creating a tab within the main window
local Tab = Window:Tab({
    title = "Preview Tab",
    icon = "rbxassetid://17654156688"
})
--[[
title = <string> - The title displayed on the tab.
icon = <string> - URL or asset ID for the icon displayed on the tab.
]]
```

## Creating a button
```lua
-- Adding a button to the tab
local Button = Tab:Button({
    title = "Preview Button",
    callback = function() print("button clicked") end
})
--[[
title = <string> - The title displayed on the button.
callback = <function> - The function to execute when the button is clicked.
]]
```

## Creating a toggle
```lua
local Toggle = Tab:Toggle({
    title = "Preview Toggle",
    callback = function(v) print(v) end
})
--[[
title = <string> - The title displayed on the toggle.
callback = <function> - The function to execute when the toggle state changes, receives the new state (true/false) as an argument.
]]
```

## Creating a slider
```lua
local Slider = Tab:Slider({
    title = "Preview Slider",
    min = 0,
    max = 100,
    default = 50,
    callback = function(v) print(v) end
})
--[[
title = <string> - The title displayed on the slider.
min = <number> - The minimum value of the slider.
max = <number> - The maximum value of the slider.
default = <number> - The default value of the slider.
callback = <function> - The function to execute when the slider value changes, receives the new value as an argument.
]]
```

## Creating a label
```lua
local Label = Tab:Label({
    text = "Preview Label"
})
--[[
text = <string> - The text displayed on the label.
]]
```

## Creating a dropdown
```lua
local Dropdown = Tab:Dropdown({
    title = "Option",
    callback = function(v) print(v) end,
})
--[[
title = <string> - The title displayed on the dropdown.
callback = <function> - The function to execute when an option is selected, receives the selected value as an argument.
]]

-- Adding an option to the dropdown
Dropdown:Add("ID", "Value", {
    title = "Option",
    callback = function(v) print(v) end,
})
--[[
ID = <string> - The identifier for the dropdown option.
Value = <string> - Just another identifier cuz im a dumbass.
title = <string> - The title displayed for the dropdown option.
callback = <function> - The function to execute when the option is selected, receives the selected value as an argument.
]]
```

## Creating a textbox
```lua
local Textbox = Tab:Textbox({
    title = "Textbox",
    default = "Input",
    callback = function(v)
        print(v)
    end
})
--[[
title = <string> - The title displayed on the textbox.
default = <string> - The default text in the textbox.
callback = <function> - The function to execute when the text changes, receives the new text as an argument.
]]
```

## Creating a keybind
```lua
local Bind = Tab:Bind({
    title = "Bind",
    bind = "E",
    key = Enum.KeyCode.E,
    hold = false,
    callback = function() print("Pressed") end
})
--[[
title = <string> - The title displayed on the key bind.
bind = <string> - The default key to bind.
key = <Enum.KeyCode> - The key code to bind.
hold = <bool> - Whether the key needs to be held down to trigger the callback.
callback = <function> - The function to execute when the key is pressed.
]]
```

## Notifying the user
```lua
local Bind = Tab:Bind({
    title = "Bind",
    bind = "E",
    key = Enum.KeyCode.E,
    hold = false,
    callback = function() print("Pressed") end
})
--[[
title = <string> - The title displayed on the key bind.
bind = <string> - The default key to bind.
key = <Enum.KeyCode> - The key code to bind.
hold = <bool> - Whether the key needs to be held down to trigger the callback.
callback = <function> - The function to execute when the key is pressed.
]]
```
