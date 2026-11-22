# Contributing to Auto Pickup

Thanks for wanting to help! You don't need to be an expert, and you don't need to ask before you start.

## Report a bug

[Open an issue](https://github.com/RHFlyer/Dead-Space-3-Auto-Pickup/issues) and say what you did, what you expected and what happened instead. Add Auto
Pickup's version and the DS3 Mod Loader's: select Auto Pickup's switch in the Mods panel and the line at the bottom
shows its version; in `ds3_mods.log`, the last line that contains "DS3 Mod Loader v" shows the loader's. Attach
`ds3_mods.log` from the game folder: Auto Pickup writes its lines there. Read a log before you post it.

If an item was collected that should have been left (or the other way round), this helps most: close the game, add
these two lines to the end of `plugins\AutoPickup\auto_pickup.ini`, play until it happens again, and attach
`ds3_mods.log`. It then lists each kind of item the mod looked at (its name and item categories, each kind once)
and what was picked up. Keep **Show the list** on: what was picked up is only logged while the list is on.

```
[debug]
log_pickup_candidates=1
```

Remove the two lines again afterwards. The file only exists once you've changed a setting in the Mods panel; if it
isn't there, create it with just those two lines.

A bug in the loader itself (the Mods panel, loading mods) belongs on the
[DS3 Mod Loader's issues](https://github.com/RHFlyer/Dead-Space-3-Mod-Loader/issues).

## Send a fix

1. Fork the repo and make a branch for your change.
2. Build it (see "Building from source" in [`README.md`](README.md)) and test it in the game.
3. Open a pull request and say what you changed and how you tested it.

Leave `ds3mod.h` as it is: it is pinned to a loader release, and the build check refuses a changed copy. Using AI to
help you is fine. Just say so in the pull request, and test what you send.

## The rules

The DS3 Mod Loader's rules apply here too, and pull requests that break them can't be accepted:

- **Only the player's own pickups.** Auto Pickup changes how your character collects items, nothing else.
- **Never touch paid DLC, entitlements, ownership, logins or the game's copy protection (DRM).**
- **No game files** and **no personal data** in the repo.

By sending a pull request you agree that your change is shared under the project's MIT licence
([`LICENSE.txt`](LICENSE.txt)).

Thanks!
RHFlyer
