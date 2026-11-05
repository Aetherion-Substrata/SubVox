# SubVox

**Natural speech from text, on your own GPU, from one 0.4 MB program.**

SubVox is a native Windows text-to-speech engine. No Python, no runtime, no
installer, no browser: one small executable talks straight to the graphics card
and writes speech to a wav file, with a timestamp for every word.

Built by Jacob at Aetherion Substrata in .lx, his own systems language.

## Speed

Measured on an RTX 5070 Ti, warm, 11 test phrases:

- **134x faster than real time**
- **First audio in 4.5 ms**
- 33 seconds of speech generated in 0.25 seconds
- Ready to speak 0.27 seconds after launch

Full table in BENCH.md.

## What you get

- `voice.exe` - the whole engine, about 0.4 MB
- `model/` - a 31M English speech model (8-bit) and tokenizer
- `voices/` - 37 ready voices
- 24 kHz mono speech, plus a word-timing file for captions, lip sync and karaoke
- Runs on any Windows 10/11 PC with a Direct3D 11 GPU

## Use

Double-click **SubVox.exe** for the window: type, pick a voice, press Enter to speak, and every word lights up as it is said. Or drive the engine from the command line with `voice.exe`:


```
voice.exe "Hello from my own engine."
voice.exe "Pick a voice." -voice Harper -out hello.wav
voice.exe -voices
voice.exe -bench
```

Each run writes the wav and `<name>.words.txt` with the start and end time of
every word.

## Licence

Apache License 2.0. See LICENSE and NOTICE for the model and voice credits.
