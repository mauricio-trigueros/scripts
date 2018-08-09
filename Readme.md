# Useful scripts for Ubuntu Server 16.04 LTS

PLAY VIDEOS : 
> mpv -vo drm video.mp4

RECORD VIDEO:
> sudo ffmpeg -t 120 -f v4l2 -framerate 25 -video_size 640x80 -i /dev/video0 output.mkv

TAKE PICTURE:
> sudo fswebcam -r 640x480 --jpeg 100 -D 3 -S 13 fswebcam.jpg

RECORD SOUND:
> arecord output.wav

VIEW BATTERY:
> acpi
