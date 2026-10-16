<p align="center"><img src="https://raw.githubusercontent.com/fdussert/fremkit/main/brand/social/fremkit-social-1280x640.png" alt="Fremkit — widget dashboard for the Corsair Xeneon Edge" width="800"></p>

# Fremkit for Homebrew

The Homebrew tap for [Fremkit](https://fremkit.app), the widget dashboard for the
Corsair Xeneon Edge on macOS. It holds one cask, which installs the signed, notarized
`Fremkit.app` from the project's [GitHub releases](https://github.com/fdussert/fremkit/releases).

## Install

```sh
brew install --cask fdussert/fremkit/fremkit
```

No separate `brew tap` is needed. macOS 13 or later, Apple silicon.

Then open Fremkit from Applications and follow the
[install steps](https://github.com/fdussert/fremkit#install-the-app): quit iCUE and Touchscreen
Gestures, and grant Input Monitoring and Accessibility when macOS asks.

## Updates

Fremkit updates itself (Sparkle, signed by the project), so the cask is marked `auto_updates` and
a plain `brew upgrade` leaves it alone. `brew upgrade --cask --greedy fremkit` forces the
update through Homebrew instead.

## Uninstall

```sh
brew uninstall --cask fremkit        # removes the app, keeps your dashboard
brew uninstall --zap --cask fremkit  # also removes ~/Library/Application Support/Fremkit and its caches
```

`--zap` deletes your dashboard, your connections and your backgrounds. Save a backup first from
**/admin → Screen → Backup** if you may come back.

## Issues

This repository only carries the cask, which the release script of the main repository writes.
Report problems, the cask's included, on
[fdussert/fremkit](https://github.com/fdussert/fremkit/issues).
