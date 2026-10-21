# Video 1 v2 · build + review

> **Note (round 5):** older stills, contact sheets and before/after sheets from rounds 1–4 showed a real-looking name and section, so they were removed and the repo history was reset. The current images are in `real-voice/` (scene-01…07, contact, contact-guides). File names mentioned in the round 1–4 notes below may no longer exist.

Final: `video-1-v2-placeholder-voice.mp4` (20.0 s, 1080×1920, ElevenLabs placeholder voice for timing only, no music).
Stills: `scene-01…07.png` · `contact.png` · `contact-guides.png` (safe area in red).
Contact sheets every 0.5 s: `review-before-*.png` (pass 1) → `review-after-*.png` (final).

## Storyboard feedback applied
1. Scene 1: broken mark → gold sparkle sticker with white die-cut edge; scratch line → full-size gold washi strip on the logo.
2. Scene 2: ID + lanyard ~35–40% bigger, straps start behind the pills, GRADE __ · SECTION pin presses on at 340 px; tagline navy with gold underline.
3. Scene 4: smiley pin separated from the class pin; all four products ~25–35% bigger.
4. All scenes: art scaled to fill the safe area (220–1500 px).

## 5 weakest things in pass 1
1. End card dead for ~1.7 s (navy + one line) before the logo landed. **Fixed**: logo slaps on "students", star + smiley pop during "para sa students", URL on "Stick-two-it".
2. Pickup pass started printing late; empty slot at 14.5 s. **Fixed**: prints from the cut.
3. End-card star sat on the period of "students." **Fixed**: moved beside the tagline.
4. Scene 2 tagline touched the ID card. **Fixed** (one-liner).
5. Tap ripple briefly covers "Order na!" text; scenes 3 and 4 open on only a headline for ~0.3 s. Not fixed.

Also fixed after pass 2: the peeling corner clipped the "!" of "stickers!" (looked like "stickers.").

## Final fixes (round 2)
1. End card: stick2it.me sticker + "Order online, pick up sa campus." land on the second "students" (17.5 s), on screen ~2.5 s. Disclaimer follows at 18.3 s.
2. Scene 2: the lanyard's built-in pin is removed (now the generic `assets/scenes/id-lanyard-no-pin.svg`), so the GRADE __ · SECTION pin is the only pin. It presses on right after "S-H-S" and squashes shut as "pwede" starts (~4.3 s), about 0.2 s earlier than before.
3. Scene 2: arrow + "section mo!" draw in right after the pin lands (4.45–4.95 s), not at the end of the scene. See `detail-scene2-pin-press.png`.
4. Scene 5: tap ripple is 80 px (was 140) and sits on the right end of the button, clear of "Order na!". See `detail-scene5-tap.png`.
Full sheets: `final-sheet-1.png`, `final-sheet-2.png`.

## Final: real voice, sound effects, demo music (round 3)
- `video-1-final-clean.mp4` — **for posting.** Real voice + sound effects, no music (music is added in TikTok).
- `video-1-final-demo.mp4` — **for showing only, never for posting.** Same, plus soundsurfer-playful under the voice, dipping while someone speaks, fading out over the last second.
- `real-voice/` — scene stills, contact sheets (`contact-guides.png` shows the safe area), before/after review sheets, `sfx-cue-frames.png` (the frame at each key sound).

**Voice.** Student recording, Bisaya-English. Pauses trimmed to 0.2 s and joined with short crossfades; two kept longer on purpose: 0.75 s after the hook question and 0.4 s after "campus", so scene 1 and scene 6 reach the 2 s minimum. Light clean-up: 80 Hz high-pass, light denoise, gentle compression, loudness to -16 LUFS. Length 20.93 s (was 20.0); the video follows the voice, nothing is sped up.

**Timing.** Whisper word timings on the joined voice; every animation is locked to the real words.
Cuts: 0–2.00 · 2.00–6.00 · 6.00–8.93 · 8.93–12.53 · 12.53–14.97 · 14.97–17.03 · 17.03–20.93 (all 2–4 s). Hook spoken by 1.24 s.

**On-screen text** now matches the student's exact script: "Tanan pwede mo-order!", "imong section!", "Imong kaugalingong pictures… himoon natong stickers!", "…apil pud ang", "Order lang online", "Dayon pick up nalang", "Gikan sa students, para sa students."

**Sound effects** (all generated in code, `build/video-1-v2/sfx.py`): soft pop on sticker slaps, paper whoosh on each cut (inside the pause, never over a word), tape rip on the washi tape, a key click per typed character, button click on "Order na!", printer whirr while the pass prints, ding on the check, click when the class pin presses on.

**Audio check**
- Loudness: clean and demo both -16 LUFS integrated, true peak about -4 dBFS → no clipping or distortion.
- Voice over SFX: at least 13.9 dB above the effects on every word.
- Voice over music (demo): at least 10.6 dB on every word, median 20 dB; music dips ~7 dB under speech (-39 vs -33 dB).
- Each effect checked against its frame (`real-voice/sfx-cue-frames.png`).

**5 weakest things (pass 1 with the real voice)**
1. Demo music almost inaudible (-39 LUFS). **Fixed**: raised 9 dB, still well under the voice.
2. Cut whooshes overlapped the first syllable of the next line. **Fixed**: each whoosh now sits inside the pause before the line.
3. Scene 4 showed only the headline for ~0.7 s ("apil pud ang" is longer than "pati"). **Fixed**: the headline lands word by word, smiley pin pops on "ang".
4. Five pops in 0.5 s in scene 5. **Fixed**: the three items inside the phone stay silent.
5. Scene 7 holds headline + logo + star for ~1.2 s before "para sa students". Not changed.
Also fixed after the wording came in: "Imong kaugalingong" wrapped to three lines (now one line at 86 px) and "imong section!" touched the ID card (now two lines).

## Text changes (round 4) — voice unchanged
1. Scene 1 hook now reads **"Taga-XU CDO ka?"**: the "uptown" sticker is replaced by a gold "CDO" word sticker in the same style (white die-cut rim, navy type, soft shadow), centered in the safe area, slapping down as "uptown" is spoken (0.58 s). See `real-voice/detail-scene1-cdo-slap.png`.
2. Scene 3 now reads **"Imong own pictures…"**, matching the voice.
Both MP4s re-rendered: 20.93 s, -16 LUFS, true peak about -4 dBFS, voice at least 13.9 dB over SFX and 10.6 dB over music on every word.

## Round 5: no real-looking names
- Scene 2 and scene 4 pin: `assets/products/class-pin-grade-section.svg` (GRADE __ · SECTION).
- Scene 2 ID: `assets/scenes/id-lanyard-no-pin.svg` (YOUR NAME · GRADE __ · SECTION).
- Scene 6 pickup pass: `assets/scenes/pickup-pass.svg` (Your Name, Grade __ - Section).
- Same voice, same timing, same positions. Re-rendered `video-1-final-clean.mp4` and `video-1-final-demo.mp4` (20.93 s each).
- Current stills: `real-voice/scene-01…07.png`, `contact.png`, `contact-guides.png`.

## Round 6: new real voice (v2)
- New recording `video-1-real-v2.mp3`: one full take, clean, no stumbles, so no line swaps. Pauses trimmed to natural beats (0.15–0.33 s; 0.74 s kept after the hook so scene 1 reaches 2 s). 80 Hz high-pass, light denoise, gentle compression, -16 LUFS. 21.44 s raw → 21.09 s.
- Whisper heard the script word for word ("sticktoit dot me" = **stick2it.me**, always written that way on screen). Script: `script-v2.md`.
  1. Taga-XU CDO ka? 2. Grade school, JHS, o SHS — pwede ka mo-order! 3. Imong own pictures, himoon natong stickers… 4. …apil pud ang pins, keychains, posters, ug prints. 5. Order lang online sa stick2it.me… 6. …dayon pick up nalang sa campus. 7. Gikan sa students, para sa students. Stick2it.me!
- Cuts: 0–2.00 · 2.00–6.00 · 6.00–8.93 · 8.93–12.63 · 12.63–15.13 · 15.13–17.17 · 17.17–21.10 (all 2–4 s). Hook spoken by 1.24 s, on screen from frame 0; CDO slaps on "CDO" (0.62 s).
- Text changes: scene 2 "Pwede ka mo-order!" (was "Tanan pwede mo-order!"), heading "Grade school, JHS, o SHS —". Scene 6 cues follow "nalang" as one word.
- End card: stick2it.me sticker lands on "para" so it is on screen 2.5 s; its corner peels on "Stick2it".

**Audio:** clean and demo both -13.9 LUFS, true peak -2.2 / -1.9 dBFS. Voice at least 11.4 dB over the effects and at least 15.1 dB over the ducked music on every word (median 27.8 dB). All six whooshes sit inside pauses.

**5 weakest things**
1. Every cut opened on an empty background for 1–3 frames (headline faded in from nothing). **Fixed**: entrances that start on a cut begin 0.15 s early while the scene is hidden. See `real-voice-v2/cuts-before-after.png` (top before, bottom after).
2. Frame 0 was blank (also in the old final and in Video 2), and "Taga-XU" punched in from 118% past the safe area. **Fixed**: frames are sampled 1 ms in; punch from 105%.
3. Scene 6 → 7 cut landed one frame late (cut time rounding). **Fixed** by the same 1 ms change.
4. End-card stick2it.me sticker and scene 4 "posters/prints" tags crossed the safe area once the slow zoom finished. **Fixed**: sticker 118 px and moved left; tags up 45 px.
5. Scene 2's gold underline under "Pwede ka mo-order!" sits ~35 px under the safe line at the end of the zoom. Not changed (decoration only).
