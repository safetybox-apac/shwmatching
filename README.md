# SH&W Matching — sound update

## Upload to your existing repository

Extract the ZIP and upload its contents to the repository root using Add file → Upload files. Commit to main and wait for GitHub Pages to redeploy. Refresh the game; its URL stays the same.

Replace index.html, app.js and config.js and add audio.js. The full package also includes the existing phone.js, phone.css, styles.css, corrected cards.csv and .nojekyll for convenience. If you have subsequently edited your scenario CSV, keep your newer copy.

## Changes

- Settings opens directly. There is no password, unlock form or editable timer.
- Every new game lasts 10 minutes, starting after the 3–2–1 countdown. Old per-device duration preferences are ignored. A game already saved in a tab retains its original deadline until finished; select Play again for a new 10-minute game.
- Background music and effects default to on. The new sound-preference key enables music on the first visit to this update, even if the old version defaulted it off. Turning music off in this version is remembered for later visits on the same browser.
- The original synthesized soundtrack now uses a melody, bass, chords and light percussion. Lobby/review music runs at 104 BPM and gameplay at 116 BPM. No external music downloads are needed.
- Browsers require user interaction before sound starts. Music begins after the first click, tap or key interaction. Enabled by default does not mean audible before that interaction.
- Music pauses when the page is hidden. The game timer continues. Settings still offers independent music and sound-effect toggles.

Desktop boards and the phone chapter picker, auto-advance, Undo, Skip, review and result views are unchanged. The real 41-card database and scoring remain intact: regular correct chapter +1; distractor in trash 0; distractor on a chapter board −2. Maximum regular-card score is 38.

There is no longer a need for a shared editable timer service in this fixed-duration edition. Each player has the same 10-minute duration but starts at their own time. No rooms, administrator, names or accounts are added.

## Validation

Local browser tests passed for both play modes, search/concept preview, placement/review/Undo, final results, small-phone layout, fixed duration despite old preferences, removal of password/timer controls, default-on audio, scheduler behavior, mute, saved sound preferences and gameplay music/effects. These are local Chromium checks; test sound on your actual phone/browser after publishing.

For a local preview, serve this directory with a web server (for example python -m http.server 8000). Opening index.html directly can prevent CSV loading.
