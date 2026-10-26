<p align="center">
  <img src="design/icon.png" width="128" alt="streampec icon">
</p>

# streampec

> A PEC-DIR control surface for macOS®, in your menu bar.

## What it does

streampec turns a button deck into a tactile control surface for your DAW, with one row of 8 buttons each for **SOLO**, **MUTE**, **REC**, and **INPUT** across up to 8 tracks. State mirrors from the DAW's change events; key presses send its setter commands. No optimistic updates: what the deck shows is what the DAW says.

## Install

1. Download the latest [DMG](https://github.com/bootlegcheeseburger/streampec-releases/releases).
2. Drag streampec into `/Applications`.
3. On first launch, accept the End User License Agreement.

Works with Pro Tools software 2025.12 or later (scripting enabled: `Preferences -> Synchronization -> Enable PTSL`) and the Stream Deck XL controller; macOS 11+.

## Configuration

streampec stores preferences as JSON in `~/Library/Application Support/streampec/config.json`:

| Field | Default | Description |
| --- | --- | --- |
| `pt_addr` | `localhost:31416` | The DAW's scripting address |
| `brightness` | `75` | Deck brightness 0-100 |
| `folder` | `print` | Folder track whose child audio tracks fill the surface; empty = all audio tracks |

Edit the file directly while streampec is closed, or use the menubar Settings submenu for brightness and folder filter.

## Privacy

Local only. streampec talks to:

- the DAW at the configured scripting address (default `localhost:31416`)
- your USB-attached deck
- `buymeacoffee.com/bootlegcheeseburger` only when you click the donate menubar item

No analytics, no auto-update, no telemetry. Full text in the EULA (`EULA.txt` in the DMG, also shown on first launch).

## Support

If streampec earned its keep, you can [buy me a cheeseburger](https://www.buymeacoffee.com/bootlegcheeseburger).

## Bug reports + feature requests

Open an [issue](https://github.com/bootlegcheeseburger/streampec-releases/issues). Source is closed; this repo accepts user-facing bug reports and feature requests only. See [SECURITY.md](SECURITY.md) for vulnerability disclosure.

## License

streampec is proprietary software. Use of the app is governed by the EULA shown on first launch (`EULA.txt` in each release DMG). © 2026 Bootleg Cheeseburger, LLC. All rights reserved.

macOS is a trademark of Apple Inc., registered in the U.S. and other countries. Pro Tools is a trademark or registered trademark of Avid Technology, Inc. Other product and company names are trademarks of their respective owners; their mention does not imply affiliation or endorsement.
