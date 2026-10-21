# Opal — Version History

## 2.6.0 — 2026-10-21
- Fixed: the screen dimmed and went to sleep in the middle of a film. Opal
  now keeps the display on while a video plays, and lets it sleep as usual
  when the video is paused, for music and on the home screen. While casting
  to a TV it keeps the Mac awake, so the stream doesn't stop when the screen
  goes dark.
- Trackpad gestures over the video: swipe sideways with two fingers to scrub
  (the picture follows your fingers and lands exactly where you stop), swipe
  up or down to change the volume. A mouse wheel steps the volume, ⇧ + wheel
  steps 5 seconds.
- Zoom to Fill: pinch out to go full screen, pinch out again and a widescreen
  film fills the whole screen instead of sitting between black bars; pinch in
  to step back. Also Z, a two-finger double tap, or View ▸ Zoom to Fill.
- Chapters on the timeline: a video's chapters show as gaps in the scrubber,
  hovering names the chapter under the pointer, and dragging near a chapter
  start lands on it exactly (with a tap on a Force Touch trackpad).
- Next and previous chapter: Playback ▸ Next / Previous Chapter (⌥⌘→ ⌥⌘←),
  or PgDn / PgUp (fn ↓ / fn ↑ on a laptop). Previous goes back to the start
  of the chapter you're in first, like a CD player's back button, and a card
  says which chapter you landed on.
- VoiceOver can read and move the timeline: it says the position, the length
  and the chapter, and swiping up or down moves 10 seconds.
- ⌘V plays what you copied: a video, song or folder copied in Finder (several
  queue up), a file path, or a link.
- Right-click Opal in the Dock to pause, skip, or pick a recent back up.
- Settings, tidied: the sidebar is split into Opal and Playback, every pane
  says in one line what it holds, and each pane runs from everyday choices to
  an Advanced section at the end (decoding, audio output). Captions are
  rewritten in plain words. Launch is now Opening Animation.
- Appearance ▸ Controls: how soon the control bar hides (Sooner, Normal,
  Later) and whether the time on its right shows the length or the time
  left. Clicking that time in the player switches it too.
- Music ▸ Record, Tape & CD: the record, tape and CD player colours, the
  mechanical sounds and the Vinyl/Tape/CD sound, which until now were only
  under the palette button on the deck.
- Settings ▸ Video ▸ Resume: Resume, Ask or Start Over for a video you
  stopped partway through. Ask starts from the beginning and shows a
  "Resume at 12:34" button for a few seconds. Under Ask and Start Over, a few
  seconds from the start no longer erases the saved spot.
- Fixed: music stuttered and the window could hang — Opal re-saved the album
  cover for the home screen many times a second while a song played. It now
  saves it once per track, off the main thread (CPU while playing a song:
  ~100% → ~25%).
- Skip Intro, Skip Recap and Skip Credits: when a video's chapters are named
  that way (Intro, Opening, OP, Recap, Credits, Ending…), a glass button
  offers to jump past them, and end credits bring the Up Next card in the
  moment they start.
- Episodes without named chapters get Skip Intro and Skip Credits too: Opal
  listens to an episode and the next one in its season folder, in the
  background and offline, and the stretch of sound they share is the theme
  tune or the closing credits, wherever it falls. A season is learned once
  and remembered. Where it can't tell, Playback ▸ Skip Intro & Credits lets
  you mark the intro and credits once for the whole folder.
- Rotation is remembered per file, like the tracks, delays, aspect and crop.
- A radio stream's current song reaches Control Center and the menu bar's
  Now Playing as it changes, not only on pause.
- Audio visualizers in step with the sound: they ran about 60 ms ahead of what
  you hear (the analysis was stamped a window early, and one layer of the
  output latency went uncounted); now a kick lands on the beat.
- A new visualizer, Glow: the cover's light spilling round its edges, with
  the bass along the bottom, the voice up the sides and the treble along the
  top, each in its own colour. Pulse splits the same way (a slow bass swell,
  a voice ripple, a treble shimmer); Ribbons are now light trails; Fluid
  throws drops off the cover on the beat — heavy ones on the bass, a spray
  on the treble — that fall back and bounce; Cymatics sits closer to the
  cover. Every style takes its colour from the cover; black-and-white covers
  stay neutral instead of turning pink.
- A new home screen, the stage: no logo — what you were watching fills the
  window (a film's frame edge to edge; a song's cover standing sharp on the right
  with its colours washed across the window), its title huge bottom-left, your
  other recents as a strip beneath it, and Open File / Folder / URL as quiet
  links. ←→ or ↑↓ bring a recent onto the stage, ↩ plays. It keeps its margins
  and tightens up in a small window.
- Living home backgrounds that answer the pointer and clicks, each in its own
  way: Opal (default — soft veils of opal colour that bloom as you move, like
  tilting the stone), Liquid Silk, Constellation and Nebula. Switch in View ▸ Home
  Background, with the ‹ › pill in the corner, or with [ and ].
- Continue now flies: the card's picture grows to fill the window (the window growing to the video's shape, or music's square, with it) and fades into the playing video; File ▸ Back to Home (⇧⌘W) shrinks the current frame back into the card. Reduce Motion cross-fades instead.
- Albums play gaplessly: the next track is queued in the player ahead of time,
  so live albums and DJ mixes run on without a gap or click between songs.
- ReplayGain (Audio ▸ ReplayGain: Album, Track or Off; Album by default, using
  the track gain when a file has no album gain) evens out loudness between songs.
- Reopening an album folder picks up at the track you were on (from its start);
  an album played to the end starts again from track one.
- An album now takes one place in Continue Watching and File ▸ Open Recent
  instead of one per track, so playing a couple of albums no longer pushes your
  videos out; opening it picks up the album where you left off. A TV series
  likewise keeps one entry (across its season folders), showing the latest episode.
- Opal can be picked in Finder's Open With ▸ Other… for MKV, WebM, FLAC and other formats on drives Spotlight indexed before Opal was installed (they were greyed out).
- Enhance Low-Resolution Video (View menu, on by default): video under 720p
  (DVD rips, old downloads, 480p streams) is cleaned up before it's enlarged —
  compression blocks and mosquito noise removed, then a trained edge-directed
  upscaler (RAVU-Lite-AR) and debanding — so it holds up on a big or 4K screen
  without the crunchy, over-sharpened look. HD is left as it is. It only runs
  when the picture is actually enlarged, and costs little (≈+5% GPU, ≈+1% CPU
  on an M5 Pro for 480p shown at 3K).
- Return (or Space) on the home screen resumes the first Continue Watching item.
- Edit the queue in the music track list: drag a track onto another to move it,
  right-click for Play Next, Remove from Queue or Show in Finder, and save the
  queue as an .m3u8 playlist (the button beside Shuffle and Repeat, or the ⋯
  menu's Save as Playlist…).
- Playback ▸ Sleep Timer: stop at the end of this track or episode, or after
  15–90 minutes; timed stops fade the sound out over the last few seconds.
- Playback ▸ Subtitle Style: Small to Extra Large, and a dark box behind the
  text for bright scenes or a TV across the room.
- Audio ▸ Music Tone: Bass Boost, Vocal Boost, Treble Boost or Spoken Word for
  music (video keeps its own mix).
- Music and video each remember their own volume, across launches — a film
  after a quiet album no longer starts at the album's level (or the reverse).
- Fixed: Night Mode never reached the player (mpv refused its filter), so it did
  nothing. It now actually evens out loud scenes and quiet dialogue.
- Press ? (or Help ▸ Keyboard Shortcuts, ⌘/) for every keyboard shortcut.
- File ▸ Open Recent ▸ Clear Menu.
- Open URL fills in a link you've just copied.
- Player-only keys (T, S, arrows…) no longer act on the welcome screen — T used
  to open Jump to Time with nothing playing.
- A launch animation, in five styles (View ▸ Launch Animation — picking one
  plays it straight away; Replay is there too, and Off):
  **Premiere** (default) — a warp through violet starlight settles, a comet
  draws the icon's lens ring, threads of light build the play mark, a pulse of
  light rings out, and the camera flies through the play button into the app.
  **Strands** — you start inside a curtain of light threads rushing past; they
  slide into place as slices of the play mark, a light sweep fuses them, and the
  camera dives back into the strands and through them into the app.
  **Projector** — a lamp strikes, its beam folds into a ring of light around the
  play mark, and the ring opens like a lens iris onto the app.
  **Hello** — a flowing mesh gradient rises out of black while "opal" is written
  by hand across it, then dissolves softly.
  **Glow** — the window's edges light up like Siri, "Opal" resolves out of a
  blur, and a rounded window of light opens from the centre.
  Plays once per launch, never when you open Opal with a file, never with Reduce
  Motion; any click or key skips to the reveal.
- Opal now appears in Finder's Open With for MKV, WebM, FLV, WMV, OGG/OGV, Opus,
  FLAC, MKA, RMVB, MTS and more — macOS has no built-in type for these, so Opal
  now declares them. It also accepts folders and .m3u playlists dropped on its
  icon, and "Make Opal the Default Video Player" covers more formats.
- New, quieter app icon: one violet, a hairline lens ring and the play mark.
- One glass look for every overlay — control bar, seek and play/pause cards,
  hints, toasts, volume, episode list, the welcome shelf — modelled on the
  system volume HUD: dark tinted Liquid Glass with a lit rim, so they match and
  stay legible over bright video.
- Seeking feedback: double-taps add up (+10s, +20s, +30s…) and the card shows
  where you'll land; ← / → (and ⇧ for 30s) now show the same card, and Space /
  Return show the play/pause card.
- The home screen rises in as the intro opens instead of underneath it.

## 2.5.1 — 2026-10-14
- New update-signing key. Copies on 2.5.0 or earlier can't install updates automatically
  any more: they show "a new version is available" with a link — install this DMG once,
  and automatic updates work again from here on.

## 2.5.0 — 2026-07-24
- Download subtitles online for videos that don't have them: pick a language
  from the captions menu (or Playback ▸ Download Subtitle) and Opal fetches a
  matching subtitle from SUBDL, saves it next to the video, and loads it right
  away — the video counterpart to online lyrics. Needs a free SUBDL API key,
  which Opal asks for once.
- Episode list for video: a season folder or playlist gets a glass side panel
  (the film-strip button in the control bar) listing every file, the current
  one highlighted — tap to jump. The Up Next card now leads by 2 minutes on
  long videos so it surfaces during end-credits, with an m:ss countdown.

## 2.4.0 — 2026-07-22
- Now runs on macOS Sequoia (15) and later — previously macOS 26 only. On older
  systems the Liquid Glass surfaces fall back to a frosted material.
- Audio visualizers for music: six styles — Nebula, Pulse, Ribbons, Fluid,
  Cymatics, and a new Waveform timeline — driven by the live audio spectrum
  (View ▸ Audio Visualizer, or ⇧⌘V to toggle)
- The Waveform timeline paints only the played portion of the track and fills
  out from the first seconds instead of starting as a thin line
- Fetch synced lyrics online for a single song or a whole album
- Refinements and fixes across music mode

## 2.3.0 — 2026-07-21
- Auto-updates via Sparkle (Opal ▸ Check for Updates…, plus a daily background check)
- Music mode: album art, synced .lrc lyrics, track list for audio files
- Continue Watching shelf on the welcome screen with poster thumbnails and resume progress
- Scrubber frame previews while hovering the timeline
- Open a whole folder or .m3u playlist as an album/queue (File ▸ Open Folder…)
- Chromecast casting alongside DLNA; Cast and Audio menus in the menu bar
- Fullscreen fixes (music view control bar, subtitle position above the bar)
- DMG distribution (`./release.sh`)

## 2.2.0 — 2026-07-20
- Chromecast support (CASTV2) next to DLNA "Play on TV"
- Playlist queue with auto-advance and Up Next card; ⇧⌘←/→ for previous/next
- Video equalizer (brightness/contrast/saturation/gamma)
- Double-tap the left/right half of the video to skip ∓10s
- Volume boost to 150%; custom volume slider
- Decluttered control bar with a ⋯ overflow menu

## 2.1.0 — 2026-07-20
- Mini player (P key or bar button): floating always-on-top window in the corner
- QuickTime-style window sizing: opens at full screen width (or height for vertical videos), aspect locked
- Subtitles lift proportionally above the bar at any window size
- Responsive control bar: compact (<700pt) and mini (<480pt) tiers; 320×180 minimum window
- A-B section loop (L), jump-to-time (T), audio delay (J/K), manual rotation (R)
- Resume where you left off (positions saved during playback)
- Combined output menu: Play on TV, audio outputs (AirPlay), screen mirroring, snapshot
- Make Opal the Default Video Player (File menu)
- yt-dlp streaming support when installed (`brew install yt-dlp`)
- Fixed: black video from a render-context race at file-open; deterministic file→window
  routing; scrubber drags no longer move the window; subtitles lift above the bar

## 2.0.0 — 2026-07-20
- Engine swapped from AVFoundation to libmpv (MPVKit, statically linked)
- Plays MKV, AVI, WebM, AV1 — everything FFmpeg decodes
- External .srt/.ass subtitles with auto-detection, subtitle delay (G/H), track switching
- Chapters menu, multi-window (one engine per window)
- Play on TV: DLNA/UPnP casting to smart TVs with a built-in HTTP media server
- AirPlay audio output switching

## 1.0.0 — 2026-07-19
- First release: native SwiftUI player with the macOS 26 Liquid Glass design
- AVFoundation engine, QuickTime-style floating controls, keyboard-driven
- Playback speed, frame stepping, snapshots, network streams, drag & drop
