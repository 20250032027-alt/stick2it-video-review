# Video 2 · Class pins "Unsa'y section ninyo?" · build + review

**Renders (placeholder voice, for timing only):**
- `video-2-clean.mp4` — voice + sound effects, no music. The version to post once the real voice is in.
- `video-2-demo.mp4` — same plus music (soundsurfer-playful), ducked under the voice, fading out over the last second. For showing only, never for posting.

24.17 s · 1080×1920 · 30 fps. Voice: ElevenLabs premade "Liam", eleven_multilingual_v2, **placeholder** — a student records the real voice from `video-2-recording.txt`, then `/video-voice`.

Storyboard stills (approved) are in this folder; build stills, contact sheets and before/after sheets are in `build/`.

## Approved changes applied
1. Scene 6 voice: "Trenta pesos ra matag pin, buy 5, get 1 free!" (the ₱30 sticker stays as the price tag).
2. Scene 7 voice and screen: "Order online, dayon pick up sa campus."
3. Scene 8 voice and screen: "Stick2It dot me, para sa mga XU CDO students!"
4. Scene 6: the pins are now big (270 px, two rows of three: 5 blue + 1 gold) with a red "FREE!" tag on the gold one; the 5 blue pins land on "pin … buy 5", the gold one and the tag on "free" with a ding.

## Timing
Cuts: 0–2.70 · 2.70–5.37 · 5.37–7.90 · 7.90–11.17 · 11.17–13.30 · 13.30–16.73 · 16.73–19.70 · 19.70–24.17.
Scenes 1–7 are all 2–4 s. The end card runs 4.47 s so stick2it.me stays up 3.8 s after "dot" (minimum 2.5 s).
Hook "Unsa'y section ninyo?" is fully spoken by ~1.0 s and on screen from frame 0.
Scene 6's placeholder line was generated at 1.15× speed so the scene stays under 4 s; the student can read it at normal pace and the cuts will follow the real voice.

## Sound
Procedural (numpy, `tools/sfx.py`): pops on slaps, a pin snap when the pin presses onto the lanyard, a printer whirr for the pickup pass, a ding on "FREE!", paper whooshes in the pauses. All 7 whooshes checked against the word timings: none overlaps a word. SFX bus sits under the voice.

## Review
Technical: nothing cut off, nothing duplicated by mistake, main content inside the safe area, on-screen text matches the voice, no real names (all pins, IDs and the pass use blanks).

5 weakest things after pass 1 (`build/review-before.png`, a frame every 0.5 s):
1. Scene 4 sat on the headline alone for ~1.2 s before "blue". **Fixed:** the three pins land on "Pili / og / kolor", then each bounces as its colour tag pops on its word.
2. Scene 6 showed only the ₱30 sticker for ~1.5 s. **Fixed:** the first pin lands on "pin", the other four on "buy 5" (now ~1 s).
3. Scene 7 opened on an empty printer slot. **Fixed:** the pass prints from the cut.
4. Scene 2 opens on just the headline for ~0.5 s before the pin lands on "design". Not fixed (short).
5. End-card URL sticker sat a little right of centre. **Fixed.**
After: `build/review-after.png`.

## What's left
- Real voice: a Bisaya-speaking student checks scene 4 ("Pili og kolor") and scene 5 ("pareha tanan"), records `voice/video-2-real.mp3`, then `/video-voice`.
- The placeholder voice is an English voice reading Bisaya, so some words sound off; it is only for timing.
