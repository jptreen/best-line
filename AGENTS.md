# Best Line project guidance

`v4.html` is the stable experimental reference. `v5.html` is the 30-second level-ramp debug build. `v6.html` is its 15-second, all-3×3 boss variant. `v7.html` is the finite 30-level motion-ramp build with no bosses and a completion survival bonus. `v8.html` inherits timed v7, makes diagonal lines level-configurable, and currently disables them throughout; `v8-notimer.html` is its static-scoring untimed counterpart. v5–v8 accept `?level=N` to start at a chosen level's first round.

## Playgrounds

- `dice-playground.html` is the reference for die shapes, colours, sizing, labels, facets, and opacity.
- `animation-playground.html` is the reference and audition space for game motion. Use it before introducing or materially changing animation in the game.
- `congratulations-playground.html` auditions v7 completion screens, compounded remaining-life bonuses, synchronized score/heart pulses, and confetti. Keep its animations manually replayable and preserve reduced-motion treatments.
- `level-playground.html` is the companion workshop for the v5 difficulty ramp. It shows editable, reorderable stages with complete playable boards, accepts a pasted trusted `LEVEL_PLAN`, and exports one with derived `fromRound` values. Use it to shape level durations, boss metadata, transition messages, scoring pressure, and independently combinable value-tick, lane-shift, and teleporter rules.
- `sound-playground.html` auditions synchronized level-complete, life-lost, and game-over audio cues. Nothing plays on load; every cue must retain its own manual replay button and matching visual feedback.

Keep animation experiments manually triggered: nothing in the animation playground should run on page load, and every behaviour must have its own replayable button. Preserve the existing-motion inventory alongside new alternatives so timing and easing can be judged against the established feel of the game.

When an audition is promoted to the game, update both `v4.html` and the playground labels so the selected/current treatment is explicit. The current selections are:

- Successful choice: directional sweep across only the selected row, column, or diagonal.
- Wrong choice: directional red ease-in; the selected line's red borders remain visible.
- Round start: five-second Early Settle opacity fade from 100% to 15% die body and 50% die label.
- V7 completion: congratulations playground Option F — Victory Sweep entrance and side confetti with “Final level cleared / You beat Likely Lines!”, no supporting sentence or BASE marker, and concise “Life bonus” wording.
- V8 sounds (timed and untimed): Glass Sparkle for a cleared level, Low Thud for a lost life, and sound playground Game Over Option C — Deep Dissolve — for an unsuccessful run end.

For motion changes, verify repeated playback, selected-line scope, final visual state, reduced-motion behaviour, console output, and narrow-screen overflow.
