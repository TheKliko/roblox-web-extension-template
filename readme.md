# <img src="images/icon-32.png.png"> Roblox Web Extension
Follow these instructions to add your mod to Roblox web

## Getting started
- Download and extract Roblox_Web_Extension_Template.zip
- Move the extracted folder to where you wish to store your extension
- Rename the folder to the name of your mod
- Open your browser and go to chrome://extensions
- Enable developer mode (top right)
- Press 'Load unpacked' and select your folder
- Your extension should now appear in your list of extensions. Underneath your extension you will see your extension ID, copy this and save it somewhere (notepad) because you will need it later

## Adding your mod
### Theme
- Go to the theme folder and replace the icons like you would with any other mod
- Go back to the root directory and open 'inject.css' in your text editor (I recommend using VSCode or Notepad++, but any other text editor will work)
- Add your theme colors at '--theme-color' and '--theme-color-solid'
  - '--theme-color-solid' can't be a gradient because it's used for things like outlined buttons and active tab indicators (eg: About/Gamepasses/Server)
    (adding a gradient anyways will result in your color becoming invisible)
  - example:
```css
--theme-color: linear-gradient(45deg,#990000, #ff0080) no-repeat;
--theme-color-solid: #cc0037;
```
- Finally, press `CTRL+F` to open the find and replace menu
  - Search for 'extensionID' and use the Replace All function to replace it with the ID of your extension

### Optional items
- Open inject.css and scroll down to line 35
-**comment**/**uncomment** different items to **disable**/**enable**  them

### Logo & popup window
- Go to the images folder and replace the icons with the logo of your mod
  - Make sure to keep the same names and dimensions
- Go to the popup folder and open index.html
  - Replace 'Template' with the name of your mod
  - Replace 'made by kliko' with whatever you want
- To change the font, open style.css and change the font-family

## Disclaimer
This extension has *not* been tested for compatibility with other extensions
This extension *will* break when Roblox decides to update their website
There are most likely more efficient methods of doing this