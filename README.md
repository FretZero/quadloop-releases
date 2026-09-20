# QuadLoop

A four-track looper plug-in for macOS and Windows. **VST3, Audio Unit, CLAP** and
a standalone app.

Built because Bitwig Studio ships no looper, and because the loopers that do
exist in a DAW tend to be one track with a fixed length. This one is four
independent slots that launch on the host's bar grid.

**Downloads are on the [Releases](../../releases) page.** This repository holds
the builds only; the source is not public.

---

## What it does

- **Four slots**, one stereo input. No routing to set up, identical in every host.
- **Host-synced launch.** Loops start and close on the bar, quantised to your
  choice of division, so tracks stay locked to each other and to the project.
- **Per-track reverse**, including reversing individual bars of a take.
- **Freeze.** Holds a short window of a loop and drones on it, so a chord
  sustains instead of going round. Two crossfaded read heads rather than a very
  short loop, which is what stops it clicking.
- **Multiply and divide** the loop length, seamlessly, while it plays.
- **Glitch** — slice a loop and let it stutter, repeat, reverse or gate.
- **Undo** on every track, and a safety limiter on the standalone.

## Installing

Download the `.pkg` from the latest release and double-click it. It installs the
VST3, Audio Unit, CLAP and standalone app, and asks for your password once
because plug-ins live in a shared folder.

Restart your music software afterwards so it rescans. Logic and GarageBand in
particular only look once per launch.

The installer is signed and notarised by Apple, so it opens without any security
warnings or Terminal steps.

### Which format

| Host | Use |
| --- | --- |
| Bitwig Studio | CLAP |
| Reaper | CLAP or VST3 |
| Ableton Live, Studio One, Cubase | VST3 |
| Logic Pro, GarageBand, MainStage | Audio Unit |
| No host at all | the standalone app |

## Betas

Releases marked **pre-release** are betas and stop recording after a date shown
under the wordmark in the plug-in. Playback keeps working past that date, so an
expired beta will not go silent in the middle of a session — it just will not
record anything new. Grab a newer build when that happens.

Projects made with a beta open in the release: the plug-in identity and the
saved-state format do not change between them.

## Reporting something

Open an [issue](../../issues) and include:

- the build, shown under the QuadLoop wordmark in the top left
- your host and its version, and whether you loaded the VST3, AU or CLAP
- your sample rate and buffer size
- what you did, and what happened instead

Timing and sync problems are worth reporting even if they sound minor. Sample
accuracy is the thing this plug-in is built around, so "it drifted slightly" is
a real bug rather than a nitpick.
