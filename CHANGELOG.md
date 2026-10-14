# Opal — Version History

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
