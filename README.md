# Learn the basics of Using Youtube Downloader

`yt-dlp` is a powerful command-line tool for downloading videos from YouTube and other platforms. It is a fork of `youtube-dl` and provides additional features and improvements.

### 1. **Installing yt-dlp**

To install `yt-dlp`, you can use Python's package manager, `pip`:

```bash
pip install yt-dlp
```

### 2. Downloading a Video
To download a video, simply run the following command:
```
yt-dlp <video_url>
```
### 3. Setting Output Filename
```
yt-dlp -o "/path/to/directory/%(title)s.%(ext)s" <video_url>
```

- `%title%` will be replaced with the video title.
- `%ext%` will be replaced with the appropriate file extension (e.g., .mp4).

```
yt-dlp <video_url>
```

### 4. Choosing Video Quality

### You can specify the quality of the video to download:

    - To download the best quality video and audio:
```
yt-dlp -f "bestvideo+bestaudio" <video_url>

```

### To download a specific resolution (e.g., 720p):

```
yt-dlp -f "bestvideo[height=720]+bestaudio/best" <video_url>

```

### 5. Downloading Audio Only

To download only the audio in a specific format (e.g., MP3):

```
yt-dlp --extract-audio --audio-format mp3 <video_url>
```

### 6. Downloading a Playlist

To download all the videos from a playlist:

```
yt-dlp <playlist_url>
```

### 7. Skipping Already Downloaded Files

If you don't want to download the same file multiple times, you can use the --download-archive option to keep track of already downloaded videos:

```
yt-dlp --download-archive downloaded.txt <video_url>
```

### 8. Using a Proxy

If you're behind a proxy, you can specify it like this:

```
yt-dlp --proxy "http://proxy_ip:proxy_port" <video_url>
```

### 9. Updating yt-dlp

To update yt-dlp to the latest version, run:

```
yt-dlp -U
```

### 10. More Options

For a full list of options and commands, you can use the --help flag:

```
yt-dlp --help
```

- This will show all the available commands and options for yt-dlp.


# Some Important Scripts

### This script will download a playlist with matching the quality and combining audio and video.

```
yt-dlp -f 136+233 --output "Downloads\Video\%(playlist_title)s\%(playlist_index)s - %(title)s.%(ext)s" <playlist link>
```



