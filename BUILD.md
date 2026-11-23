# Building the installer

The editable source is provided in `Supply-Tracker-1.0.0-Source.zip` on the release page. Extract it, then run `node build.mjs` from its root on Windows with Node.js and .NET Framework 4.x C# compiler installed.

The archive contains the mod scripts, installer source, test fixtures, branding assets and the bundled UE4SS files/license. It does not contain the game's native textures, model experiments, process dumps or save files.

The installer build runs its transaction self-test. Lua behavioral tests used during development are included under `tests`; they require the `fengari` package and test both frame-based and timer fallback updates. After installing that test dependency, run `node tests/run.mjs` from the extracted root. The development workspace command is `node nearby-supplies/tests/run.mjs`.

Validation for 1.0.0: installer transaction fixtures, English/Thai HUD fixtures, empty/usable crates, distance boundaries, stable marker updates, menu/travel lifecycle and UI scaling. In-game acceptance came from the 0.1.2 candidate; official runtime differs only in its version banner.
