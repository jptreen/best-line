# Best Line working notes

`v4.html` is the stable experimental reference. `v5.html` is the 30-second level-ramp debug build; `v6.html` is its 15-second, all-3×3 boss variant; `v7.html` is the finite 30-level motion ramp with no bosses and a completion survival bonus. `v8.html` inherits timed v7, makes diagonal lines level-configurable, and currently disables them throughout; `v8-notimer.html` is its static-scoring untimed counterpart. v5–v8 accept `?level=N` to start a run at that level's first round.

Use `dice-playground.html` for the dice visual language and `animation-playground.html` for all animation exploration. The animation playground is a durable project reference: audition motion there before changing the game, keep every animation behind an individual manual replay button, and retain the existing-motion examples for comparison.

Use `congratulations-playground.html` to audition v7 completion screens, compounded remaining-life bonuses, synchronized score/heart pulses, and confetti. Keep every treatment manually replayable and preserve its reduced-motion alternative.

Use `level-playground.html` to design and compare the v5 difficulty ramp. It provides editable, reorderable stages and full playable boards, imports trusted pasted plans, derives `fromRound` from each stage duration, and exports combined motion rules, level-advance copy, timer, life-pressure, and boss metadata into a draft `LEVEL_PLAN`.

Use `sound-playground.html` to audition synchronized level-complete, life-lost, and game-over cues. Nothing should play on load; keep every cue behind its own manual replay button with the matching visual feedback. Both V8 variants use Glass Sparkle for a clear, Low Thud for a lost life, and Game Over Option C — Deep Dissolve — for an unsuccessful run end.

When a treatment is selected, update both the game and playground. Current v4 motion choices are a directional success sweep limited to the chosen line, a directional wrong-choice ease-in whose red borders remain, and the five-second Early Settle round-start opacity fade.

The selected v7 completion treatment is congratulations playground Option F: Victory Sweep entrance and side confetti with “Final level cleared / You beat Likely Lines!”, no supporting sentence or BASE marker, and concise “Life bonus” wording.

Test animation changes for clean replay, correct row/column/diagonal scope, stable end states, reduced-motion handling, console errors, and responsive overflow.
