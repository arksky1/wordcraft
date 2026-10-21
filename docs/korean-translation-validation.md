# Korean translation validation

Catalog additions against `e3bb06a298c24f96678c3c513fa19dbf630ccab6`: **151** entries. Every existing Korean entry is preserved. Only translations supplied by the root task were used.

## Independent coverage

- Restored 129 root-supplied keys previously omitted because an unmerged third-party PR also proposed them. These keys are included in this branch; no unmerged PR is required to supply them.
- The third-party PR patches were used to identify overlap, not as translation sources.
- The correction ZIP contains 153 direct-lookup mappings. All 153 keys and root-provided values were verified against their current source locations.
- Correction ZIP SHA256: `a97cb9c22e110d177ca7a5f0a70db976aee34056ae030fca2c3d9a0e884f755f`.

## Static checks

- Catalog syntax/table shape, unique keys, source keys, named placeholders, trailing ellipses, explicit shortcut tokens, and preservation of all existing Korean entries passed.
- Tokenized source audit: 899 unique direct translation lookup keys; 7 word-bearing keys still missing from this catalog.
- Recorded 242 dynamic lookup sites for source inspection. Variable document text, file names, and machine identifiers retain their existing behavior.
- Finite dynamic checks passed: PhotoCraft menu catalog (632 keys), VectorCraft render-site table (21 keys), FigCraft English UI (1,747 keys), required command reference (574 keys), and menu reference (31 keys). All accepted root-supplied context/id/plural keys resolve.
- `git diff --check` passed.

## Checks not run

Cargo, rustc, and rustfmt are unavailable. Rust installation remains awaiting user approval; no tools were installed. The following were not run:

- `cargo test -p wordcraft-ui-egui`
- `cargo fmt --all --check`
- `cargo clippy -p wordcraft-ui-egui --all-targets -- -D warnings`
- `cargo xtask layers`, `cargo xtask assets`, `cargo xtask wasm`, and `cargo xtask ci`
- Native/web UI rendering, layout, runtime switching, and font/glyph coverage

Static checks do not replace runtime verification or prove coverage of arbitrary runtime-generated messages.

## Remaining root input needed

These live direct calls are absent from both supplied root inputs. No new translation was generated:

- `Current Document` (`crates/ui-egui/src/canvas.rs:2592`)
- `Select a place in this document:` (`crates/ui-egui/src/dialogs.rs:2338`)
- `Top of the Document` (`crates/ui-egui/src/dialogs.rs:2343`)
- `Bookmarks` (`crates/ui-egui/src/dialogs.rs:2363`)
- `Discard the recovery copy of {name}?` (`crates/ui-egui/src/dialogs.rs:2708`)
- `This cannot be undone. Your original file stays unchanged.` (`crates/ui-egui/src/dialogs.rs:2709`)
- `Discard` (`crates/ui-egui/src/dialogs.rs:2713`)
