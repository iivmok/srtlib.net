srtlib.net
============================

A set of C#/.NET APIs for:
 - Reading .srt files
 - Modifying times
 - Writing .srt files
 - Getting subtitles at a specific time.

### Usage
```C#
var srt = new SRTFile("test.srt");
var time = new TimeSpan(1, 45, 10);
var subtitles = srt.GetSubtitlesAt(time); //Subtitles that should be displayed at 1:45:10
srt.Multiply(0.95904); //23.976 -> 25.000 fps
srt.Subtitles[0].Text = "hello, world!";
srt.WriteToFile("test2.srt");
```
