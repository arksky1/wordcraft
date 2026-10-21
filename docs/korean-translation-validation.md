# Korean translation validation

Catalog additions against `e3bb06a298c24f96678c3c513fa19dbf630ccab6`: **22** entries. Existing Korean entries are unchanged. The provided translation data was checked against the current Rust sources; candidate keys with no matching production literal were excluded. No new translations were generated.

## Static checks

- Catalog structure, unique keys, original key preservation, named placeholders, trailing ellipses, and explicit shortcut tokens checked with Python 3.14.5.
- Existing catalog entries were compared with the baseline commit.
- New entries have source-location evidence in the local audit; dynamic labels use the existing translation paths.
- `git diff --check` passed.

## Checks not run

Cargo, rustc, and rustfmt are unavailable in this environment. Rust installation is awaiting user approval; no tools were installed. The following checks have **not** been run:

- `cargo test -p wordcraft-ui-egui`
- `cargo fmt --all --check`
- `cargo clippy -p wordcraft-ui-egui --all-targets -- -D warnings`
- `cargo xtask layers`, `cargo xtask assets`, `cargo xtask wasm`, and the full `cargo xtask ci` gate
- Native and web UI rendering, layout, runtime language switching, and font/glyph coverage

## Candidate filtering

- Excluded 16 supplied candidate keys without a matching production source literal.
- Excluded 129 supplied keys already proposed in open Korean translation PRs.

- https://github.com/storytold/wordcraft/pull/1946
- https://github.com/storytold/wordcraft/pull/1987
- https://github.com/storytold/wordcraft/pull/2064
