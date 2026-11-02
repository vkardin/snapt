# Privacy Policy

_Last updated: November 2, 2026_

This policy covers the Snapt desktop app and the Snapt browser extension for
Chrome, Edge and Firefox.

## The short version

Snapt does not collect, store or share any personal data. It has no servers,
no accounts, no analytics and no ads. Your screenshots stay on your device
until you choose to save, copy or share them.

## Browser extension

The extension works entirely inside your browser:

- Screenshots and images are processed locally and are never sent anywhere.
- It keeps no history or settings outside your browser and does not track the
  pages you visit.
- The only network request it makes is downloading an image you asked to save
  as PNG or JPG, from the site that image comes from.

What its permissions are used for:

| Permission | Why |
| --- | --- |
| Access to all sites | Taking a screenshot of the page you are on, area selection, full-page capture and the Alt+click image viewer |
| `contextMenus` | The "Save image as PNG / JPG" menu items |
| `downloads` | Saving screenshots and converted images to your computer |
| `scripting` | Starting a screenshot in tabs that were open before the extension was installed |
| `offscreen` (Chrome only) | Converting SVG images to PNG or JPG |

All code, including the WebAssembly editor, ships inside the extension
package. No code is loaded from the internet.

## Desktop app

The app works offline. It connects to the internet only in two cases:

- **Update check.** It asks the GitHub API for the latest release and, when
  you agree to update, downloads it from GitHub Releases. You can turn
  automatic checks off in Settings.
- **Search image.** If you choose to search a screenshot on Google Lens, that
  screenshot is sent to Google. This happens only when you pick that action,
  and Google's privacy policy applies to it.

Settings, logs and crash reports are stored only on your computer.

## Changes

Any change to this policy will be published in this file, together with the
date above.

## Contact

Questions? Open an issue at https://github.com/vkardin/snapt/issues.
