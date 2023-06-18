# Whisper TUI
Quickly generate and search transcriptions of audio.

## Rationale

- quickly find stuff in a podcast
- uses `tiny.en` model by default for fast transcriptions good enough for searching
- uses SQLite FTS5 for good enough search

## Example Usage

### Why I Made This Thing in the First Place

```
$ wget https://www.podtrac.com/pts/redirect.mp3/traffic.libsyn.com/secure/cortex/Cortex_142.mp3
$ ./whisper-tui Cortex_142.mp3
Detected language: English
100%|███████████████████████████████████████████████████████████████████████████████████████████████| 511979/511979 [02:16<00:00, 3743.42frames/s]
> physics
0:38:42.080000 - 0:38:48:  I highly recommend you get a physics degree. And one of the main reasons for that is that
0:38:49.280000 - 0:38:55.920000:  people with a physics degree are just highly in demand in the world of employment. Like I know
0:40:47.520000 - 0:40:52.880000:  immediately translate all the physics stuff here. And if there's something that they're doing in a
0:43:26.160000 - 0:43:30.480000:  Yeah. And again, that's like just straight from a bunch of physics stuff is like, oh, you know,
0:38:30.240000 - 0:38:37.360000:  the deal with this branch? So long time listeners will know I am a big booster of getting a physics
```

### Dig Through a YouTube Video
```bash
yt-dlp -x --audio-format mp3 -o audio.mp3 $URL; ./whisper-tui audio.mp3
```
