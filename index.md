![QuickLook icon](https://cloud.githubusercontent.com/assets/1687847/26008086/060d9cca-374c-11e7-9345-7f0f0f91a421.png)

[![license](https://img.shields.io/github/license/xupefei/QuickLook.svg)](https://www.gnu.org/licenses/lgpl-3.0.en.html)
[![AppVeyor](https://img.shields.io/appveyor/ci/xupefei/QuickLook.svg)](https://ci.appveyor.com/project/xupefei/QuickLook)
[![Github All Releases](https://img.shields.io/github/downloads/xupefei/QuickLook/total.svg)](https://github.com/xupefei/QuickLook/releases)
[![GitHub release](https://img.shields.io/github/release/xupefei/QuickLook.svg)](https://github.com/xupefei/QuickLook/releases/latest)

*This project is currently under heavy development. Come back often to see what's new.*

<img src="http://pooi.moe/QuickLook/sample.gif?2" width="400">

## Background
[Quick Look](https://en.wikipedia.org/wiki/Quick_Look) is among the few features I missed from Mac OS X. It enables *very* quick preview of file by pressing <kbd>Space</kbd> key while highlighting it, without opening its associated application. Then I decide to add this feature to Windows by myself, which results this “QuickLook” project.

You may ask, why you write this when there several alternatives available on the Internet (e.g. [WinQuickLook](https://github.com/shibayan/WinQuickLook) and [Seer](https://github.com/ccseer/Seer))? The answer is that, they are all among those which no longer actively developed, lack of support of file types and plugins, or asking user for amounts of $$$.

## Usage

### General usage

 1. Download either installer or portable archive from [GitHub Release](https://github.com/xupefei/QuickLook/releases) page
 2. Run `QuickLook.exe`
 3. Select a file/folder on the Desktop / in a File Explorer window / in an Open- or Save-File dialog
 4. Press <kbd>Spacebar</kbd>
 5. Select another file/folder in the same manner
 6. When you're done, click on the `❎` button, or press <kbd>Spacebar</kbd> again

### Hotkeys

 - <kbd>Spacebar</kbd> Show/Hide the preview window
 - <kbd>Esc</kbd> Hide the preview window
 - <kbd>Enter</kbd> Open/Execute current file
 - <kbd>Mouse️</kbd> <kbd>↑</kbd> <kbd>↓</kbd> <kbd>←</kbd> <kbd>→</kbd> Preview another file
 - <kbd>Ctrl-Wheel</kbd> Zoom in/out images

### Integration

 - You may set up a custom hot key that fires event `QuickLook.exe C:\path\to\your\file.txt`. 

## Development

The previewing ability can be extended by new plugins. Read the [plugin interface](https://github.com/xupefei/QuickLook/blob/master/QuickLook/Plugin/IViewer.cs), [context object](https://github.com/xupefei/QuickLook/blob/master/QuickLook/Plugin/ContextObject.cs) for more information. [Out-of-box plugins](https://github.com/xupefei/QuickLook/tree/master/QuickLook.Plugin) contain more detailed implementation.
Note that any plugin must be under the `QuickLook.Plugin` namespace, has the filename similar to `QuickLook.Plugin.YourPlugin.dll` and placed under `<Application>\Plugins\QuickLook.Plugin.YourPlugin\` subfolder.

## Licenses

![GPL-v3](https://www.gnu.org/graphics/gplv3-127x51.png)

Application icons made by Freepik from www.flaticon.com. Used under the [Flaticon Basic License](http://file000.flaticon.com/downloads/license/license.pdf).

All source codes, except which are from other projects mentioned in “Related projects” section, are licensed under [GPL-3.0](https://opensource.org/licenses/GPL-3.0).

If you want make any modification on these source codes while keeping new codes not protected by GPL-3.0, please contact me for a sublicense instead.

