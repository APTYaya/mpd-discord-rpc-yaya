# MPD Discord RPC — Yaya’s Fork

> **Personal fork of the original project:**  
> **https://github.com/JakeStanger/mpd-discord-rpc**  
> This fork lives at: **https://github.com/APTYaya/mpd-discord-rpc-yaya**

This is a customized version of the MPD Discord RPC client with additional code for extracting album art, preparing metadata for missing MusicBrainz releases. 

# What is changed in this fork? 

### 1. Missing MusicBrainz / Cover Art Archive Detection
When a track is played, this fork checks:

- If it has a MusicBrainz Release ID  
- If Cover Art Archive has front cover art  
- If the track cannot be found on MusicBrainz at all  

### 2. Automatic Embedded Album Art Extraction
If MusicBrainz/Cover Art Archive doesn’t have artwork:

- The fork attempts to extract embedded album art from the audio file using `ffmpeg`.
- Extracted images are saved locally as JPEGs.

Few things I still need to fix but since this is mainly for personal usage probably will not fix anytime soon, 
But if someone does want to change this inside album_art.rs just change these two consts.

const MUSIC_ROOT: &str = "/mnt/main/Music"; 
const PENDING_MB_QUEUE_DIR: &str = "/home/Yaya/.local/share/mpd-rpc/pending_covers";

To whatever path you have for your music directory and whichever path you want the pending music brainz queue to be. 



