# Minifox Theme

A clean, distraction-free Firefox theme that automatically hides toolbars when not in use, featuring rounded UI elements and smooth animations.

## Features

- **Auto-hiding toolbars**: Toolbars fade out when not hovered or focused
- **Rounded UI elements**: Modern rounded corners on address bar and search elements
- **Smooth animations**: Elegant transitions for showing/hiding toolbars
- **Fullscreen compatibility**: Proper behavior in fullscreen mode
- **Custom tab icons**: Optimized tab icon sizing
- **Sidebar enhancements**: Improved sidebar styling with shadows

## Installation Instructions

### Step 1: Enable Custom Stylesheets

1. Open Firefox and type `about:config` in the address bar
2. Click "Accept the Risk and Continue" if prompted
3. In the search box, type: `toolkit.legacyUserProfileCustomizations.stylesheets`
4. Double-click the setting to change it from `false` to `true`
5. You should see the value change to `true` (in bold)

### Step 2: Find Your Firefox Profile Directory

#### On Windows:
1. Press `Windows + R` to open the Run dialog
2. Type: `%APPDATA%\Mozilla\Firefox\Profiles\`
3. Press Enter
4. You'll see a folder with a name like `xxxxxxxx.default-release-xxxxxxxxxxxx`

#### On macOS:
1. Open Finder
2. Press `Cmd + Shift + G` (or go to Go → Go to Folder...)
3. Type: `~/Library/Application Support/Firefox/Profiles/`
4. Press Enter
5. You'll see a folder with a name like `xxxxxxxx.default-release-xxxxxxxxxxxx`

#### On Linux:
1. Open your file manager
2. Navigate to: `~/.mozilla/firefox/`
3. You'll see a folder with a name like `xxxxxxxx.default-release-xxxxxxxxxxxx`

### Step 3: Create the Chrome Directory

1. Open the profile folder you found in Step 2
2. Create a new folder named exactly `chrome` (all lowercase)
3. This folder should be at the same level as files like `prefs.js`, `places.sqlite`, etc.

### Step 4: Install the Theme

**Option A: Git Clone (Recommended)**
1. Open terminal/command prompt
2. Navigate to your profile's `chrome` folder
3. Run: `git clone https://github.com/yourusername/minimal-auto-hide-theme.git .`
4. This will clone the repository directly into your chrome folder

**Option B: Copy Single File**
1. Download the `userChrome.css` file from this repository
2. Copy the `userChrome.css` file into the `chrome` folder you created

Your folder structure should look like this:
```
Profile Folder/
├── chrome/
│   ├── userChrome.css
│   └── (other files if using git clone)
├── prefs.js
├── places.sqlite
└── (other Firefox files)
```

### Step 5: Restart Firefox

1. Close Firefox completely
2. Reopen Firefox
3. You should see the auto-hiding toolbars in action!

## How to Use

- **Hover over the top of the browser** to show toolbars
- **Press F6 or Ctrl+L** to focus the address bar (toolbars will appear)
- **Click in the address bar** to show toolbars
- **Move your mouse away** to hide toolbars again
- **Press ESC** to hide the URL bar if it's not disappearing automatically
- **Fullscreen mode** will show toolbars normally

## Customization

You can customize the theme by editing the CSS variables at the top of `userChrome.css`:

```css
:root {
  --toolbar-height: 40px;     /* Height of toolbars */
  --tab-icon-size: 20px;      /* Size of tab icons */
  --border-radius: 10px;      /* Roundness of UI elements */
}
```

## Troubleshooting

### Theme not working?
1. Make sure `toolkit.legacyUserProfileCustomizations.stylesheets` is set to `true` in `about:config`
2. Verify the `chrome` folder is in the correct profile directory
3. Check that `userChrome.css` is in the `chrome` folder
4. Restart Firefox completely

### Toolbars not hiding?
1. Make sure you're not in fullscreen mode
2. Try hovering over the very top of the browser window
3. Check if any extensions are interfering

### Visual glitches?
1. Try refreshing the page (F5)
2. Restart Firefox
3. Check if you have other themes or extensions that might conflict

### Find your profile directory easily:
1. Open Firefox
2. Go to `about:profiles` in the address bar
3. Look for the profile marked as "Default" (in use)
4. Click "Open Folder" next to "Root Directory"

## Updating

**If you used git clone:**
1. Navigate to your profile's `chrome` folder in terminal/command prompt
2. Run: `git pull`
3. Restart Firefox

**If you copied the file manually:**
1. Download the latest `userChrome.css` file
2. Replace the existing file in your `chrome` folder
3. Restart Firefox

## Uninstalling

To remove the theme:
1. Delete the `chrome` folder from your profile directory (this removes all theme files)
2. Restart Firefox
3. Optionally, set `toolkit.legacyUserProfileCustomizations.stylesheets` back to `false` in `about:config`

## Support

If you encounter issues:
1. Check the troubleshooting section above
2. Make sure you're using a recent version of Firefox
3. Try disabling other extensions temporarily
4. Create an issue on the GitHub repository

## Browser Compatibility

- Firefox 60.0 or later
- Tested on Firefox 115+
- May work on Firefox-based browsers (Waterfox, LibreWolf, etc.)

## License

This theme is open source and available under the MIT License.

---

**Note**: This theme modifies Firefox's user interface. While it's safe to use, always backup your profile directory before making changes, and be aware that Firefox updates may occasionally break custom themes. 