# Using Snapt

Everything Snapt can do, key by key. For a short overview, see the [README](../README.md).


Press **PrtSc** (**Cmd+Shift+9** on macOS) or pick **Take screenshot** in the tray menu.
For a whole long page, press **Ctrl+Shift+PrtSc** (**Cmd+Shift+0** on macOS) and click the
browser window; see [scrolling screenshots](#scrolling-screenshots) below.
The screen freezes, then:

| Action | How |
| --- | --- |
| Select an area | Drag with the left mouse button |
| Select a window | Point at it and click |
| Move or resize it | Drag inside the selection or by its handles |
| Select the whole screen | `Ctrl+A` |
| Pick a drawing tool | Click it in the panel, or press `P` pen, `L` line, `A` arrow, `R` rectangle, `E` ellipse, `M` marker, `T` text, `N` numbered step, `B` pixelate, `U` blur, `H` spotlight |
| Crop the selection | `C`, then drag the new area inside it; drawings stay |
| Type an exact size | Type digits, `X` and digits again, then `Enter`, e.g. `800x600` (image pixels; `Esc` gives up) |
| Nudge the selection | Arrow keys move it by a pixel, with `Shift` by 10; with `Alt` they resize it |
| Filled rectangles and ellipses | `F` switches filling on and off |
| Move or delete a shape | With no tool picked, drag it, or click it and press `Delete` |
| Straight lines, squares | Hold `Shift` while drawing |
| Line width, text size | Mouse wheel |
| Undo, redo | `Ctrl+Z`, `Ctrl+Y` or `Ctrl+Shift+Z` |
| Copy to clipboard | `Ctrl+C`, `Enter` or double-click the selection |
| Save to a file | `Ctrl+S` |
| Print | `Ctrl+P` |
| Search for similar images | `Ctrl+F` |
| Copy the text in it | `Ctrl+Shift+C` |
| Pin it on top of all windows | `F3` |
| Scrolling screenshot of the selection | `Ctrl+Shift+S`; Snapt scrolls the page itself |
| Record a video of the area | `Ctrl+Shift+R`; `Enter` stops, `Esc` cancels |
| Pick a color from the screen | `I`, then click; the HEX code is copied too |
| Cancel | `Esc` or right-click |

On macOS, use `Cmd` instead of `Ctrl`. While typing text, `Enter` starts a new line and
`Esc` finishes the text.

A pinned screenshot stays on top of other windows. Drag it to move it, zoom it with the mouse
wheel or `+` and `-` (`0` goes back to 100 %), copy it again with `Ctrl+C`, save it with
`Ctrl+S`, and close it with `Esc`, a double click or the middle mouse button.

## Scrolling screenshots

For a scrolling screenshot of a whole page, press `Ctrl+Shift+PrtSc` (`Cmd+Shift+0` on macOS)
or pick **Scrolling screenshot of a page** in the tray menu, then click the browser window or
select the part of the page to capture. In an open screenshot, `Ctrl+Shift+S` or the scroll
button does the same for the selection (or the window under the mouse). Snapt goes to the top
of the page, scrolls it down by itself and stops at the end; a panel next to the area shows the
height so far, `Enter` or a click on it finishes early, and `Esc` cancels. The result is copied
and pinned so you can check it and save it with `Ctrl+S`.

Move the mouse to take over and scroll by hand; if the panel says you went too fast, scroll back
up a little. Where Snapt can't turn the wheel itself (on Wayland, or on macOS until Snapt is
allowed under *System Settings > Privacy & Security > Accessibility*), it asks you to scroll by
hand. Sticky headers and footers appear once, but floating buttons and the scroll bar repeat
down the image, so select the page without them for the cleanest result; pages that change as
they scroll (animations, infinite feeds) may not glue.

## Video and the tray menu

To record a video, select an area and press `Ctrl+Shift+R` or the camera button. Snapt records
10 frames a second, for up to two minutes; the panel shows the time. Press `Enter` or click
the panel to stop and choose where to save it: MP4 if `ffmpeg` is on the `PATH`, GIF always.

On Windows the tray menu is Snapt's own: icons next to every item, the shortcuts, the delays
as buttons, and the update right inside, in the system's light or dark theme; arrow keys
and `Enter` work too. On macOS and Linux it is the system menu with the same icons, since
there the menu bar or the desktop draws tray menus itself.

The tray menu also has:

- **Scrolling screenshot of a page**: the same as `Ctrl+Shift+PrtSc` above;
- **Copy full screen**: all monitors at once, straight to the clipboard;
- **Repeat last area**: opens the screenshot with the area you selected last time;
- **Screenshot with delay**: in 3, 5 or 10 seconds, to catch menus and tooltips;
- **Recent screenshots**: the last 10, kept between restarts; click one to pin it. Set a
  **Pin last screenshot** shortcut in the settings to pin the newest one from anywhere;
- **Check for updates**: looks right away and shows the result in the menu, or offers
  **Update to Snapt X.Y.Z** at the top when a new version is out.

## Settings

Pick **Settings…** in the tray menu. There you can:

- switch the language: English, Russian or Ukrainian (it follows the system by default);
- on **Shortcuts**, give every action its own keys: capture, color picker, full screen,
  repeat last area, scrolling screenshot of a page, and copy text, scrolling screenshot,
  recording, pin, copy and save on the open
  screenshot. Click a field and press the keys; Backspace clears it. Snapt tells you when
  the keys are already taken;
- on **Features**, turn off text recognition, scrolling screenshots, pinning, image search,
  printing, video recording or the color picker; their buttons and shortcuts go away;
- on **Editor**, turn off any drawing tool, from the pen to blur, spotlight and crop; it
  leaves the toolbar and its key stops working. Crop starts turned off;
- let Snapt replace the system screenshot tool: on Windows, PrtSc and Win+Shift+S open Snapt
  instead of the Snipping Tool, Snapt can be picked for the `ms-screenclip` and
  `ms-screensketch` links (Windows asks you to confirm that one), and Snapt either asks first
  or replaces it on its own; turning the option off gives everything back; on GNOME, the shortcut opens Snapt instead of GNOME Screenshot, on Wayland too; on
  macOS and other desktops, the window explains the one manual step;
- choose the screenshots folder and format, save without a dialog, also save what you copy,
  open a file once it is saved, and start at login;
- copy shots as an image or as a file, ready to paste straight into a folder in Explorer,
  Finder or your file manager;
- keep Snapt up to date: it checks GitHub Releases once a day and offers **Update** in the
  tray and in the window. The Windows installer, the macOS app and the AppImage update
  themselves; for the `.deb`, the download page opens.

The settings are stored in a plain-text `settings.ini` in the config folder. Two more
settings live only there: `history` sets how many recent screenshots to keep (0 keeps none),
and `file_name` sets how saved files are named, with `strftime` codes such as `%Y` year,
`%m` month, `%d` day, `%H` hour, `%M` minute and `%S` second. The default is
`Snapt_%Y-%m-%d_%H-%M-%S`.

## Command line

`snapt --capture` takes a screenshot right away, `snapt --pick` opens the color picker and
`snapt --settings` opens the settings.
If Snapt is already running, that copy does it, so the command can be bound to a key in the
system settings, for example on Wayland desktops without a global shortcuts portal.

`snapt --logs` opens the folder with the log of the last run (`snapt.log`) and a
`crash-<time>.txt` report for each crash. Attach them to a bug report.

## Platform notes

- **macOS:** the first capture asks for the Screen Recording permission in
  System Settings → Privacy & Security. Restart Snapt after allowing it.
- **Linux:** the tray icon uses the StatusNotifierItem protocol. KDE supports it out of
  the box; on GNOME, install the AppIndicator extension. Text recognition uses Tesseract:
  `sudo apt install tesseract-ocr tesseract-ocr-rus tesseract-ocr-ukr`.
- **Wayland:** Snapt takes screenshots and gets its shortcut through the desktop portal
  (xdg-desktop-portal). The first time, the desktop may ask you to allow screenshots and
  to confirm the shortcut; you can change the key later in the desktop's keyboard
  settings. Global shortcuts need a portal that has them, such as KDE Plasma 6 or
  GNOME 48 and later. Elsewhere, bind `snapt --capture` to a key in the keyboard settings.
- **Windows:** text recognition works for the languages added in Settings → Time & language
  that include it.
