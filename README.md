# mp4_player
mp4 js player based on broadway decoding

For creating a new video-button, it's need to convert video by ffmpeg utility and appropriate console command:

```- ffmpeg -y -i input.mp4 -r 30000/1001 -b:a 2M -bt 4M -vcodec libx264 -pass 1 -coder 0 -bf 0 -flags -loop -wpredp 0 -an output.mp4```

* repeatmode - it can takes values «off» and «hand».
    * «off» - replay is off, 
    * «hand» - manual replay will active. By default, auto-repeat is on.
* videopixels - JSON-parameters for videopixel. Example:
'[
      { "StartPosition": 0.0, "EndPosition": 0.05, "TrackingLink": "https://goo.gl/PedWM5" },
      { "StartPosition": 0.25, "EndPosition": 0.5, "TrackingLink": "https://goo.gl/PedWM5" },
      { "StartPosition": 0.5, "EndPosition": 0.75, "TrackingLink": "https://goo.gl/PedWM5" },
      { "StartPosition": 0.75, "EndPosition": 0.95, "TrackingLink": "https://goo.gl/PedWM5" },
      { "StartPosition": 0.95, "EndPosition": 1, "TrackingLink": "https://goo.gl/PedWM5" }
    ]' 
