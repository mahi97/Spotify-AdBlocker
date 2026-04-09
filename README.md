# Spotify Ad Blocker

> Listen to [Spotify](https://www.spotify.com) on macOS — without ads.

Spotify Ad Blocker is a lightweight AppleScript utility that detects when Spotify plays an advertisement and responds automatically. Choose from three modes: silently mute ads, swap them with your local Music library, or make them disappear entirely by playing your own tracks in their place.

---

## Requirements

- **macOS** (uses AppleScript / `osascript`)
- **Spotify** desktop application
- **Music** application (required for `swap` and `rm` modes)

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/mahi97/Spotify-AdBlocker.git
   cd Spotify-AdBlocker
   ```

2. Create a symbolic link so the command is available system-wide:

   ```bash
   ln -s "$(pwd)/spotify-ad" /usr/local/bin/spotify-ad
   ```

---

## Usage

Run one of the following commands in your terminal while Spotify is open:

| Command | Description |
|---|---|
| `spotify-ad mute` | Mute ads automatically, unmute when they end |
| `spotify-ad swap` | Mute ads and play your current Music track instead |
| `spotify-ad rm` | Play your Music track seamlessly through the ad break, then resume Spotify |
| `spotify-ad` | Show available commands |

---

## Modes

### `mute`
Monitors the currently playing Spotify track. When an advertisement is detected, the volume is set to zero and restored once the ad is over.

### `swap`
When an ad starts, Spotify is muted and the Music app begins playing your current track. When the ad ends, Music pauses and Spotify audio is restored.

### `rm` (remove)
Provides the most seamless experience. When an ad is detected, Spotify is muted and your Music track plays in its place. Once the Music track finishes, Spotify is automatically unmuted and resumes playback — as if the ad never happened.

---

## How It Works

The script polls the Spotify AppleScript interface every 0.5 seconds. It detects advertisements by checking whether the string `:ad:` appears in the current track's Spotify URL — a reliable indicator of ad playback used by Spotify's internal track metadata.

---

## Roadmap

- [x] Mute mode
- [x] Swap mode
- [x] Remove mode
- [ ] Configurable polling interval
- [ ] Launchd/autostart support
- [ ] Notification Center alerts

---

## Similar Projects

| Project | Platform | Language |
|---|---|---|
| [blockify](https://github.com/mikar/blockify) | Linux | Python |
| [spotify_ad_blocker_linux.rb](https://github.com/superr4y/hacks/blob/master/spotify/spotify_ad_blocker_linux.rb) | Linux | Ruby |
| [spotify-blacklist-mute](https://github.com/ysangkok/spotify-blacklist-mute) | Linux | Bash |
| [Spotify-AdKiller](https://github.com/SecUpwN/Spotify-AdKiller) | Linux | Bash |

---

## License

This is free and unencumbered software. Do whatever you want with it.
