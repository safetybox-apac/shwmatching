# SH&W Matching — Desktop and Phone

## Update your existing GitHub Pages site

1. Extract the ZIP.
2. Open your repository → Code → Add file → Upload files.
3. Upload the extracted files directly to the root and commit to main. Replace index.html, app.js, styles.css, config.js and cards.csv; add phone.js and phone.css. Keep .nojekyll. README.md is documentation only.
4. Wait for Pages to redeploy and reload the website. Your Pages settings and website URL remain unchanged.
5. Hard-refresh or open a private window if the old page remains. An existing saved game resumes in its original mode; finish it and select Play again to reach mode selection.

The corrected real database is included: 41 cards, 19 chapters, 38 regular scenarios and 3 distractors. The sample banner is disabled. Assignments and scoring are preserved.

## Phone experience

The home page offers Play on Desktop and Play on Phone, with icons. The appropriate option is suggested by screen width, but players can select either. Instructions and a 3–2–1 countdown follow.

Desktop retains movable Post-it boards. Phone shows one scenario at a time:

- Choose chapter opens a searchable panel. Search by number, chapter name or concept. Select a chapter, inspect its concept, then confirm placement.
- The next unanswered card appears immediately. Correctness stays hidden until the end.
- Trash places the card in the trash and advances.
- Skip leaves the current choice unchanged and moves to another unanswered card.
- Undo reverses the last placement and returns to that card. If revising an answer, Undo restores its previous destination. One Undo step survives refresh.
- Review lists cards and their chosen destinations. Filter to unanswered cards or select any card to revisit. Checkmarks mean answered, not correct.
- After all cards are placed, review them or finish. Finish game requires confirmation. Timeout finishes automatically and closes open pickers.

Normal phone play fits one screen, tested at 390×844 and 320×568. The card area can scroll for long text, enlarged fonts or short screens. Chapter/review lists scroll within their panels. The timer and action controls stay outside the reading area.

Phone results show one card at a time, the player's choice, points, Previous/Next and Reveal correct answers. Correct placements are green, incorrect red and unanswered gray. Desktop keeps board-style results.

## Content and scoring

The real distractors describe unsafe practices. Instructions now tell players to discard incorrect or unsafe practices even when they mention a safety topic.

Correct chapter +1; wrong chapter, regular card in trash or unplaced 0; distractor in trash 0; distractor on a chapter board −2. Maximum score is 38; scores can be negative. Both modes share the same scoring function.

Keep the five CSV headers exactly:

`Chapter Ref,Chapter Name,Concept,Card #,Post-it Card Scenario`

Use unique Card # values and preserve references as text, including 7.1 and 7.2. Repeat the same chapter name and concept for each chapter reference. Continue editing the sheet and replacing its CSV export as needed. Resumed games retain their original data snapshot until finished.

## Shared timer connection still pending

This package upgrades the phone/desktop experience. It does NOT implement the shared settings backend. The existing 10-minute default and safetybox gate remain; changing duration in the dialog still affects only this browser/device and future games. Do not treat it as an all-player setting.

The separately requested all-player duration control still needs the shared Apps Script/Sheets connection discussed earlier. It has not been configured or deployed. Changing defaultMinutes in config.js only changes the default for browsers without a saved preference. Each player has an individual start/deadline.

The static-site password is a convenience gate, not secure authentication. No player names, rooms or account system are introduced. Session storage supports same-tab recovery; the timer continues through refresh, settings and backgrounding.

## Sound, hosting and verification

Music/effects remain under Settings beside AIRBUS. Audio is generated locally. No external font, picture or music host is needed. For local preview, use a web server such as python -m http.server 8000 and open http://localhost:8000; double-clicking index.html can block CSV loading.

Local Chromium checks passed for mode selection, all 41 cards, phone viewport fit, search and concepts, automatic advance, Undo including revised placements, trash, Skip, review filters, resume/deadline, timeout with picker open, results/reveal, all-placed screen and desktop boards. Phone screenshots were visually inspected. No browser JavaScript errors were recorded.

This package has not been uploaded to your repository. Test the deployed site on your actual phones and work network before the session.
