# Security Policy

## Supported versions

Only the latest released version of streampec receives security fixes.

## Reporting a vulnerability

Please do not open a public GitHub issue for security problems.

Use GitHub's private advisory channel:
[Report a vulnerability](../../security/advisories/new)

Or email: security@bootlegcheeseburger.com

I aim to acknowledge reports within 72 hours. As a solo maintainer, fix
turnaround depends on severity and availability; expect days to weeks
rather than hours.

## Scope

In scope:

- The streampec macOS app distributed via this repo's GitHub Releases.
- The notarized DMG (verify the stapled signature with `spctl -a -t open --context context:primary-signature -v streampec-v*.dmg`).

Out of scope:

- Third-party dependencies (report upstream; I'll bump after their fix).
- Issues requiring physical access to an unlocked machine.
- macOS, Pro Tools, or Stream Deck firmware bugs.

## What streampec touches

- Speaks the Pro Tools PTSL gRPC API at a user-configured host:port (default `localhost:31416`).
- Opens a USB-attached Elgato Stream Deck XL via HID.
- Stores preferences in `~/Library/Application Support/streampec/` as JSON. No `UserDefaults` use, no Keychain use, no remote storage.
- Reaches out to `https://www.buymeacoffee.com/bootlegcheeseburger` only when the user explicitly clicks the menubar donate link.
- No analytics, no auto-update, no telemetry.

The app is sandbox-disabled (USB HID access isn't sandbox-safe), but ships with Hardened Runtime + Developer ID signature + notarization.
