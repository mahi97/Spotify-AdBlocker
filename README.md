#Spotify Ad Blocker (for MacOS)

Listen to [Spotify](https://www.spotify.com) - without ads!


We all Love Spotify, but also hate Ads.
With this script you can listen to spotify without having to listen to ads.

You can automaticlly mute ads, or swap them with your itunes music or play your music when ad is started and resume spotify after your local music finished like there's no ad at all!

### Installation

Get the latest Version of `Spotify-AdBlocker`:

    git clone https://github.com/mahi97/Spotify-AdBlocker.git

move to folder of Spotify-AdBlocker

    cd Spotify-AdBlocker

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

- `mute`       : mute Spotify, unmute when ad is over
- `swap`       : mute Spotify, play itunes current track, stop and unmute when ad    is over
- `rm (remove)`: mute Spotify, play itunes current track, stop and unmute when track is over

### TODO

- [ ] Modes
  - [x] swap   mode
  - [x] remove mode
  - [ ] Intel  mode 
- [ ] Test needed
- [ ] Add manual mode
- [ ] Select Itunes Playlist

### Similar Projects


- [blockify](https://github.com/mikar/blockify) - automatic/blacklist-based ad-blocker written in Python
- [spotify_ad_blocker_linux.rb](https://github.com/superr4y/hacks/blob/master/spotify/spotify_ad_blocker_linux.rb) - automatic ad-blocker written in Ruby
- [spotify-blacklist-mute](https://github.com/ysangkok/spotify-blacklist-mute) - blacklist-based muting, written in Bash
- [Spotify-AdKiller](https://github.com/SecUpwN/Spotify-AdKiller) - automatic ad blocker, written in bash fot linux

### License

Take it, it's yours :)
