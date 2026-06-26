# mySanitas x Amigo, AI Agent Demo (for the Keralty call)

A self-playing demo reel showing an Amigo AI agent across two scenes Keralty cares about:

1. **Patient experience (mySanitas app)**: opens with the real onboarding carousel
   ("Welcome to your new care experience!" hero plus page dots), then memory and personalization,
   lab results explained, conversational booking plus intake, red-flag triage that escalates to a
   clinician, compliance framing. The chat uses the app's floating-bubbles-on-blue style, with
   white result/booking cards on top so they stay readable.
2. **Emergency Dept "Super Scribe"**: ambient bedside documentation, prior-doctor alert,
   clinical-protocol enforcement, note pushed to eClinicalWorks.

Runs about 2 minutes, then holds on a closing card.

## Design
- **Framing (title, scene intros, recap, closing cards) uses the Amigo brand** pulled from the
  `/design` skill: warm light background, Flecha S display serif, ABC Diatype Mono eyebrows,
  Inter body, orange `#AA412A` accent, blue `#083241` for data. Real Amigo logo + Flecha S /
  Diatype Mono font files live in `assets/`.
- **The phone screens keep the Sanitas brand** (their app): Sanitas blue, mint-green chat
  bubbles, butterfly logo, radial home, matched to the real app screenshots.
- **No icons and no em dashes anywhere** (per the Amigo design Safety Net).
- Closing stats use vetted gtm-repo claims: 80+ organizations, first agent live in ~6 weeks,
  100% clinical safety performance; compliance stated as HIPAA, SOC 2 Type II, GDPR.

## Play it on the call
1. Open `index.html` in **Chrome** (keep the `assets/` folder next to it). Use the browser's own
   full screen (View > Enter Full Screen, or Cmd+Ctrl+F) for an edge-to-edge picture.
2. Click **Play demo**. It runs start-to-finish on its own (about 1 min 40 sec).
3. **Controls** (move the mouse to reveal them):
   - **Pause / Play** button, bottom-left. Spacebar also toggles.
   - **Scrubber** along the bottom edge: click or drag to **rewind** or jump to any moment.
   The controls stay hidden while the mouse is still, so they won't show in a recording.

> All fonts (Inter, Flecha S, Diatype Mono) and the Amigo logo load from `assets/` via relative
> paths, so the demo is fully self-contained and works offline, including from `file://`. No
> internet required on the day. Just keep the `assets/` folder next to `index.html`.

## Turn it into an .mp4 (to drop into a deck / share)
On macOS:
1. Open `index.html` in Chrome, go full screen.
2. Press **Cmd+Shift+5**, choose Record, then click Play.
3. Let it run, stop the recording. The `.mov` lands on your Desktop; convert to `.mp4` if needed.

(Tip: do not move the mouse so the controls stay hidden during recording.)

## Customizing
- All content and timing is in the `<script>` block in `index.html` (search for `SCENE 1` / `SCENE 2`).
- Amigo framing tokens and Sanitas app tokens are CSS variables at the top of `index.html`.
- Captions are the lower-third lines (`setCaption(...)`). Edit text there.
- Patient/clinician names, lab values, appointment slots are inline in the scene code.
