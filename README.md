# Roblox UI Library

This script provides a customizable UI library for Roblox exploit development. The library allows you to create windows, tabs, buttons, toggles, and sliders. It is based on Roblox's UI system and integrates features such as draggable windows and smooth animations. This script is modular, making it easy to add new components as required.

## How to Use

1. **UI**
   To use the Lib, you need to use
   ```
   https://raw.githubusercontent.com/GamerGBG/Roblox-UI-LIB/refs/heads/main/UI-LIB.lua?token=GHSAT0AAAAAACVXFDHT6VB23MUARIOYQVO2ZXP5ZXQ
   ```

1. **Window Creation**
   To create a window, call the `Library:Window("Title")` function. This will spawn a new window with the specified title.
   ```lua
   local Window = Library:Window("My Window")
   ```

2. **Tab Creation**
   Use the `Window:Tab("Tab Name")` function to add tabs to your window.
   ```lua
   local Tab = Window:Tab("Main Tab")
   ```

3. **Adding Buttons**
   To add buttons inside a tab, call `Tab:Button("Button Name", function)` where the function is the callback executed when the button is clicked.
   ```lua
   Tab:Button("Click Me", function()
       print("Button clicked!")
   end)
   ```

4. **Adding Toggles**
   You can add toggles with `Tab:Toggle("Toggle Name", callback)`. The callback returns `true` when the toggle is activated and `false` when it's deactivated.
   ```lua
   Tab:Toggle("Enable Feature", function(state)
       if state then
           print("Feature enabled!")
       else
           print("Feature disabled!")
       end
   end)
   ```

5. **Adding Sliders**
   Sliders can be added with `Tab:Slider("Slider Name", min, max, default, callback)`. The callback provides the slider's current value.
   ```lua
   Tab:Slider("Volume", 0, 100, 50, function(value)
       print("Volume set to " .. value)
   end)
   ```

## Additional Features

- **Drag-and-Drop**: The window is fully draggable. Users can click and drag the window from the top bar to reposition it.
- **Collapsing/Expanding Window**: The window has a minimize button in the top-right corner that smoothly collapses or expands the window with animations.
- **Tab Highlighting**: Tabs are highlighted upon selection and automatically switch content when clicked.

## Example Usage

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamerGBG/Roblox-UI-LIB/refs/heads/main/UI-LIB.lua?token=GHSAT0AAAAAACVXFDHT6VB23MUARIOYQVO2ZXP5ZXQ",true))()
local Window = Library:Window("My Cool Exploit")
local MainTab = Window:Tab("Main")
local SettingsTab = Window:Tab("Settings")

MainTab:Button("Print Hello", function()
    print("Hello World!")
end)

SettingsTab:Toggle("Enable God Mode", function(state)
    if state then
        print("God Mode Activated")
    else
        print("God Mode Deactivated")
    end
end)

SettingsTab:Slider("Speed", 0, 100, 50, function(value)
    print("Speed set to", value)
end)

local Window = Library:Window("My Cool Exploit")
local MainTab = Window:Tab("Main")
local SettingsTab = Window:Tab("Settings")

MainTab:Button("Print Hello", function()
    print("Hello World!")
end)

SettingsTab:Toggle("Enable God Mode", function(state)
    if state then
        print("God Mode Activated")
    else
        print("God Mode Deactivated")
    end
end)

SettingsTab:Slider("Speed", 0, 100, 50, function(value)
    print("Speed set to", value)
end)
```
