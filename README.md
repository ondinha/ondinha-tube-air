# Ondinha Tube Air

**High-frequency exciter with a tube stage: adds warm even or bright odd harmonics above a frequency, under the untouched signal. Oversampled, no aliasing.**

A VST3 and Audio Unit plug-in from [Ondinha](https://github.com/ondinha), a DAW 2.0: native AI tools combined with traditional sound engineering tools.

Adds air and presence the way an exciter does: by creating **new** harmonics in the highs instead of just boosting them. A tube stage makes them thick and warm (even harmonics) or bright and edgy (odd), and they sit under your original signal, which is never touched.

Louder hits get richer harmonics, so it follows the music instead of adding hiss.

## What it's good for

- Master: a touch of tube air from 5 kHz up.
- Vocals: thick presence around 2.5 kHz.
- Cymbals: silk instead of brightness.
- Guitars: bite with odd harmonics.

## Controls

| Control | Range | What it does |
|---|---|---|
| Freq | 1-12 kHz | Harmonics are made from what's above this. |
| Drive | 0-24 dB | How hard the tube stage is hit. |
| Even (tube) | 0-100 % | Warm even harmonics vs bright odd ones. |
| Amount | 0-100 % | How much of the harmonics is added. |
| Smooth | 6-20 kHz | Low-pass on the harmonics. |
| Listen | Mix / Harmonics only | Hear just what's being added. |
| Output | +-12 dB |  |

## Presets

Built in as host programs (your DAW's preset menu):

- Master: tube air
- Vocal: thick presence
- Cymbals: silk
- Guitars: bite

## Download and install

Builds will be on the [Releases](../../releases) page.

**macOS:** copy `Ondinha Tube Air.vst3` to `~/Library/Audio/Plug-Ins/VST3` and `Ondinha Tube Air.component` to `~/Library/Audio/Plug-Ins/Components`, then rescan plug-ins in your DAW.

| Format | Platform |
|---|---|
| VST3 | macOS |
| Audio Unit (AU) | macOS |

Works in any VST3 or AU host: Ableton Live, Logic Pro, Reaper, Bitwig Studio, Cubase, Studio One, FL Studio and others.

## How it works

A parallel exciter (Aphex Aural Exciter lineage): high-pass, drive, an asymmetric tanh tube curve (the bias sets the even harmonics), then the curve's clean part is subtracted so only new overtones stay, high-passed again and smoothed. The tube stage runs 4x oversampled with linear-phase filters, so harmonics don't fold back as aliasing. **Amount 0 is bit-transparent.** Latency reported to the host.

## More Ondinha plug-ins

- [Ondinha Bus Comp](https://github.com/ondinha/ondinha-bus-comp): Console-style glue compressor for the mix bus and groups.
- [Ondinha Split EQ](https://github.com/ondinha/ondinha-split-eq): Transient / tonal split EQ: separate gain for the attack and the sustain in every band.
- [Ondinha Limiter](https://github.com/ondinha/ondinha-limiter): True-peak brickwall limiter for mastering, with an optional oversampled clipper.
- [Ondinha Unmask](https://github.com/ondinha/ondinha-unmask): Spectral side-chain ducking: dips a track only at the frequencies where the key is loud, only while it plays.
- [Ondinha Resonance](https://github.com/ondinha/ondinha-resonance): Dynamic resonance tamer for harsh mixes, vocals and guitars: pulls down narrow peaks only while they ring and leaves the broad tone alone.
- [Ondinha Imager](https://github.com/ondinha/ondinha-imager): Multiband stereo imager with mono low end: width for lows, mids and highs on phase-matched Linkwitz-Riley crossovers.
- [Ondinha Delay](https://github.com/ondinha/ondinha-delay): Tempo-synced stereo / ping-pong delay with filtered, saturated feedback and ducking, so the echoes stay out of the way of the vocal.
- [Ondinha Graphic EQ](https://github.com/ondinha/ondinha-graphic-eq): 10-band octave graphic EQ with analog-matched bells (31 Hz - 16 kHz, +-12 dB).

## Feedback

Found a bug or a host where it misbehaves? [Open an issue](../../issues) with your DAW, its version and your OS.
