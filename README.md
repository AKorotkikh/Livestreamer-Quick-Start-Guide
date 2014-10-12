#TL;DR
1. Download VLC, rtmpdump and Livestreamer binaries
2. Put VLC and rtmp inside the Livestreamer folder (in this guide: **livestreamer\vlc** and **livestreamer\rtmpdump**)
3. Create a .cmd file inside the Livestreamer folder with following contents (**replace twitch.tv/... with any other Twitch link**):
```
livestreamer twitch.tv/... source --rtmpdump=rtmpdump\rtmpdump.exe --player="vlc\vlc.exe --file-caching=10000" --player-passthrough=http,hls,rtmp
```
4. Start the .cmd file you just created to watch the stream.

#Binaries:
**Livestreamer**(windows): http://livestreamer.readthedocs.org/en/latest/install.html - **Zip archive** link  
**VLC**(windows): https://www.videolan.org/vlc/download-windows.html - any of the two archived 32-bit packages  
**rtmpdump**(windows): https://rtmpdump.mplayerhq.hu/download/rtmpdump-2.4-git-010913-windows.zip  

#Stream link format
Livestreamer supports many different streaming services, not just Twitch (full list at http://livestreamer.readthedocs.org/en/latest/plugin_matrix.html).  
All links have similar format: **host**(without http://) **quality**. For twitch, the quality can be set to: source, high, medium, etc. (depends on the particular stream).   
To get all quality options, first run the following command from inside the Livestreamer folder (or create a second .cmd file):

```
livestreamer twitch.tv/...
OR
livestreamer youtube.com/watch?v=...

```
For Twitch, **source** quality is available on all streams.

#Player settings
This guide uses VLC binaries for maximum compatibility with file cache set to 10 seconds for less buffering.

#Why?  
###Why download binaries separately?  
To keep all the dependencies in one folder for portability.  
###Why this guide?
This is a simple guide to get you up and running as quickly as possible, I still recommend you to read the official docs for Livestreamer.
