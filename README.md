#Spotify Ad Blocker (for MacOS)

Party with [Spotify](https://www.spotify.com) - without ads!


We all love Spotify, but sometimes people (like us) want to focues on "Coding" without having to listen to interrupting ads before having bought [Spotify Premium](https://www.spotify.com/premium/). Well, with this project, now you can!

**This is for testing purposes ONLY!** Spotify is a fantastic service and worth every penny. This script is **NOT** meant to circumvent buying premium! Please do consider switching to premium to support Spotify 


### Installation

**Automated Installation**

Get the latest Version of `Spotify-AdBlocker`:

    git clone https://github.com/mahi97/Spotify-AdBlocker.git

Run the provided installer:

    cd Spotify-AdBlocker
    ./install.sh


**Manual Installation**


make a symbolic link into `/usr/local/bin/`:

```bash
ln -s $(pwd)/spotify-ad /usr/local/bin/spotify-ad
```

### Usage


* To run spotify-ad in mute mode, type `spotify-ad mute`
* To run spotify-ad in swap mode, type `spotify-ad swap`
* To run spotify-ad in rm   mode, type `spotify-ad rm`
* To show a list of these commands, just type `spotify-ad`.


**Modes**


- `simple`: mute Spotify, unmute when ad is over
- `interstitial`: mute Spotify, play random local track, stop and unmute when ad is over
    + If the local track is shorter than the ad, `Spotify-AdKiller` will automatically try to loop it. This will only work with players that support a loop option. If you are planning to use this feature with a custom player make sure to also supply a custom loop option in your configuration file.
- `continuous`: mute Spotify, play random local track, stop and unmute when track is over
    + You can skip the local track as soon as the ad is over. To do so, simply press Play or Forward/Next in your Spotify client (or use the corresponding hotkeys).
    + Please note that the `continuous` ad blocking mode works best with tracks that are longer than the average ad duration (≈30-45s). If a custom track ends prematurely or is shorter than the current ad, `Spotify-AdKiller` will switch to the next random local track in line.

The default ad blocking mode is `continuous`.

`Spotify-AdKiller` will always fall back to `simple` mode if no local tracks are found and/or if no supported music player is available on the system.


### Similar Projects



- [blockify](https://github.com/mikar/blockify) - automatic/blacklist-based ad-blocker written in Python
- [spotify_ad_blocker_linux.rb](https://github.com/superr4y/hacks/blob/master/spotify/spotify_ad_blocker_linux.rb) - automatic ad-blocker written in Ruby
- [spotify-blacklist-mute](https://github.com/ysangkok/spotify-blacklist-mute) - blacklist-based muting, written in Bash

### License

Take it, it's yours :)