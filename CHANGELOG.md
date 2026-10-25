# BetterZoom v2.4.2

## Changed

- Zoom sound replaced: **Spyglass use** plays when zooming in (`resources/spyglass_zoom_in.wav`,
  44.1 kHz mono, peak-normalized). The zoom-out sound was removed.
- New **Zoom Sound** toggle and **Zoom Sound Volume** slider (0-1) in the mod menu / `config.json`
  (`zoomSound`, `zoomSoundVolume`).

## Fixed

- JNI local references leaked on every zoom (the game thread never returns to Java to free them).
- `settings()` returned a reference to a temporary; it now returns by value.
- SoundPool is no longer kept (or leaked) when the WAV files fail to load, and load errors are cleared.
- No more sound cut off / played while the mod is being disabled or unloaded.

# BetterZoom v2.4.1

## Fixed

- Zoom and the cinematic bars no longer stop working when another mod is installed.
  Previously, with BedrockTools also loaded, the zoom button responded but the world never
  zoomed and the bars never appeared.
- BetterZoom no longer interferes with other mods that hook the same game function.

## Install

1. In the launcher, **delete the old BetterZoom package first** — this build keeps the `2.4.1`
   version string, so it collides with the previous package of the same name.
2. Import **`BetterZoom_v2.4.1.levipack`**.
