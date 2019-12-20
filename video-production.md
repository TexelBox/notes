#VIDEO PRODUCTION

---

- here I will outline my process for recording, editing and uploading videos to YouTube.

- tools: OBS, OpenShot, ffmpeg

-  OBS settings:  
save recordings (no space, hyphens, lowercase) in obs-raw folder.  
.mkv output  
x264 encoder  
1920x1080 (base/canvas & output/scaled)  
Lanczos scaling  
60fps  
CBR of 15000 (15Mbps)  
keyframe interval of 2seconds  
veryfast CPU usage preset  
HIGH profile  
audio bitrate: 320kbps  
48khz sample rate  
stereo


1. create an OBS source (e.g. window capture)
2. if capture doesn't fill entire area, then snap the viewbox to bottom of screen so that black bars are on top.
3. record the source, which will export an .mkv file

- OpenShot settings:  
profile: HD 1080p 60fps (1920x1080)  
48000 sample rate  
stereo (2 channel)  

4. create a new OpenShot project, set profile/prefs if needed  
5. import .mkv file(s)
6. remove some uneeded tracks or add more
7. drag files onto timeline, if trimming needs to be performed, use the current time dragger tool + right click and "keep left" or "keep right"
8. once everything is lined up starting at 0seconds, export (don't write extension in filename), make sure that the profile and advanced settings match OBS recording (e.g. 15.0Mb/s video bitrate and 320kb/s audio bit rate)

- ffmpeg settings:  
simply place the path to \bin in PATH variable

9. apply the following command to make the exported .mp4 from OpenShot into faststart (web-ready) - moov atom gets moved to start of .mp4  
ffmpeg -i openshot-export.mp4 -acodec copy -vcodec copy -movflags faststart yt-upload.mp4

10. upload yt-upload.mp4 on YouTube, configure meta data appropriately









---