# <img src="images/icon-32.png"> Roblox Web Extension Template
Follow these instructions to add your mod to <a href="https://www.roblox.com">roblox.com</a>



## Getting started
- Download and extract Roblox_Web_Extension_Template.zip
- Move the extracted folder to where you wish to store your extension
- Rename the folder to the name of your mod
- Open your browser and go to `chrome://extensions`
- Enable developer mode
- Press <kbd>Load unpacked</kbd> and select your folder
- Your extension should now appear in your list of extensions. Underneath your extension you will see your extension ID, copy this and save it somewhere (notepad) because you will need it later



## Adding your mod
### Theme
- Go to the theme folder and replace the icons like you would with any other mod
- Go back to the root directory and open `inject.css` in your text editor (I recommend using VSCode or Notepad++, but any other text editor will work)
- Add your theme color to the variables at lines 29 and 30
  - <var>--theme-color-solid</var> can't be a gradient because it's used for things like outlined buttons and active tab indicators (eg: About/Gamepasses/Server).
    Adding a gradient anyways will result in your color becoming invisible,
    if you used a gradient for your main color I recommend using its average color.
  - example:
    ```css
    --theme-color: linear-gradient(45deg,#990000, #ff0080) no-repeat;
    --theme-color-solid: #cc0037;
    ```
- Finally, press <kbd>CTRL</kbd>+<kbd>F</kbd> to open the find and replace menu
  - Search for <var>extensionID</var> and use the Replace All function to replace it with the ID of your extension

### Optional items
- Open `inject.css` and scroll down to line 35
- <kbd>comment</kbd> / <kbd>uncomment</kbd> different items to <kbd>disable</kbd> / <kbd>enable</kbd>  them

### Logo & popup window
- Go to the images folder and replace the icons with the logo of your mod
  - Make sure to keep the same names and dimensions
- Go to the popup folder and open `index.html`
  - Replace 'Template' with the name of your mod
  - Replace 'made by kliko' with whatever you want
- To change the font, text color or background: open style.css and change the font-family
  - example:
  ```css
  --background: linear-gradient(45deg, #000000, #222222) no-repeat;

  --header-color: linear-gradient(0deg, #888, #fff, #888) no-repeat;
  --header-font: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

  --footer-color: #fff;
  --footer-font: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  ```



## Disclaimer
This extension has *not* been tested for compatibility with other extensions
This extension *will* break when Roblox decides to update their website
There are most likely more efficient methods of doing this