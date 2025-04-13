# Modern Glassmorphic Firefox Theme - Setup Guide

This guide will help you install and customize your new Firefox theme with rounded corners, glassmorphic effects, gentle animations, and a beautiful new tab experience.

## Installation Steps

### 1. Enable userChrome.css in Firefox

1. Open Firefox and type `about:config` in the address bar
2. Accept the warning message
3. Search for `toolkit.legacyUserProfileCustomizations.stylesheets`
4. Set it to `true` by double-clicking on it

### 2. Find Your Firefox Profile Folder

1. In Firefox, go to `about:support`
2. Look for "Profile Folder" and click "Open Folder" or "Show in Finder" (Mac)
3. This opens your Firefox profile directory

### 3. Create Required Folders and Files

1. In your profile folder, create a new folder called `chrome` if it doesn't exist
2. Inside the `chrome` folder, create the following structure:
   ```
   chrome/
   ├── assets/
   │   ├── backgrounds/
   │   ├── fonts/
   │   └── icons/
   ├── userChrome.css
   ├── userContent.css
   └── new-tab.js
   ```

### 4. Copy the Files

1. Copy the contents of the `userChrome.css`, `userContent.css`, and `new-tab.js` files into the corresponding files in your chrome folder
2. Update file paths in all files by replacing `YourUsername` and `YourProfile` with your actual Windows username and Firefox profile name

### 5. Download Required Assets

#### Fonts
Download the Inter font:
1. Visit [Google Fonts - Inter](https://fonts.google.com/specimen/Inter)
2. Download the font family
3. Extract and place the `Inter-Regular.woff2` and other weights in the `chrome/fonts/` folder, renamed to `inter.woff2`

#### Background Images
For the backgrounds folder, download high-quality images and name them according to the list in `new-tab.js`:
- `morning-mist.jpg`
- `marble-soft.jpg`
- `gradient-calm.jpg`
- `soft-clouds.jpg`
- `abstract-flow.jpg`

You can find good quality images on [Unsplash](https://unsplash.com/), searching for terms like "marble", "soft gradient", "misty landscape", etc.

#### Icons
For the icons folder, download icons for common websites or use a favicon service. Place them in the `chrome/assets/icons/` folder, matching the names in the script:
- `google.png`
- `youtube.png`
- `gmail.png`
- `github.png`
- `twitter.png`
- `netflix.png`
- `amazon.png`
- `reddit.png`
- `add.png` (a simple plus icon)

### 6. Restart Firefox

Close Firefox completely and restart it for the changes to take effect.

## Features Overview

### New Tab Experience

Your new tab page now includes:

- **Clock & Date**: Large, elegant time display with full date
- **Quick Access Speed Dial**: Customizable grid of your favorite sites
- **Todo List**: Persistent task list that syncs between tabs
- **Dynamic Background**: Click the refresh button (↻) in the top-right of the clock area to cycle through backgrounds

### Browser UI Improvements

- **Vertical Tabs**: Tabs are now displayed vertically on the left side for better organization
- **Glassmorphic Effects**: Semi-transparent UI elements with blur effects
- **Rounded Corners**: All UI elements have modern, rounded corners
- **Animations**: Gentle animations for interactions and transitions
- **Address Bar Enhancements**: The address bar animates to center when focused
- **No Close Buttons**: Tab close buttons are hidden (use Ctrl+W instead)
- **Removed Elements**: Bookmark star and "Loaded from extension" text are hidden

## Customization

### Changing Colors

To change the color scheme, edit the `:root` variables at the top of both CSS files:

```css
:root {
  --glass-bg-light: rgba(245, 245, 250, 0.65);
  --glass-bg-dark: rgba(35, 35, 45, 0.65);
  --accent-primary: rgba(100, 130, 200, 0.9);
  --accent-secondary: rgba(140, 160, 210, 0.8);
  /* other variables */
}
```

### Customizing the Speed Dial

The speed dial will initially load with default sites. To customize:
1. Click the "Add New" tile
2. Enter the website name and URL when prompted
3. Your new site will appear in the grid

### Managing Tasks

- Add tasks by typing in the input box and pressing Enter
- Mark tasks as complete by clicking the checkbox
- Delete tasks by hovering over a task and clicking the "×" button

## Troubleshooting

If the theme doesn't appear correctly:

1. Verify that `toolkit.legacyUserProfileCustomizations.stylesheets` is set to `true`
2. Check that all file paths in the CSS files are correct for your system
3. Make sure all required folders and files are in the correct locations
4. Restart Firefox completely (close all windows and reopen)

If specific elements don't look right:

1. Firefox updates might change element IDs or classes
2. You might need to update selectors in the CSS files
3. Use Firefox's inspector (F12) to identify the correct elements

## Known Features and Limitations

- **New Tab Functionality**: The custom new tab relies on JavaScript injection which may be affected by Firefox security updates
- **Vertical Tabs**: This implementation uses CSS to transform standard tabs; for more functionality, consider a dedicated extension
- **Multiple Address Bars**: This design creates the illusion of multiple bars through styling
- **Performance**: Glassmorphic effects may impact performance on older systems; reduce `--backdrop-blur` values if needed

## Credit and Resources

This theme was created as a custom design combining various modern UI principles:
- Glassmorphic design
- Neumorphism
- Microsoft's Fluent Design
- Apple's Human Interface Guidelines

For more Firefox customization resources:
- [r/FirefoxCSS](https://www.reddit.com/r/FirefoxCSS/)
- [Firefox Source Docs - UserChrome](https://firefox-source-docs.mozilla.org/devtools-user/settings/index.html)

Enjoy your new, beautiful Firefox experience!
