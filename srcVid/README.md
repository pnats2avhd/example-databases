To create your own test-SRCs with numbered frames:

```bash
ffmpeg -f lavfi -i testsrc=duration=6:size=384x216:rate=60 \
-vf "drawtext=fontfile=/usr/share/fonts/truetype/ubuntu-font-family/UbuntuMono-R.ttf:\
text=%{n}:fontsize=72:r=60:x=(w-tw)/2: y=h-(2*lh): fontcolor=white: box=1: boxcolor=0x00000099" \
-c:v ffv1 numbered-video.avi
```

You can change duration, size and rate in the first row to whatever you want to test. Remember to match the rate in the video filter as well, so the numbering is correct. 
The current command line would produce a 6 second long file with 360 frames, with a 384x216 pixel resolution
