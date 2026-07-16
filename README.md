# StrengthOS Movement Catalog

The public, versioned movement and equipment vocabulary used by StrengthOS.

## Files

- `movements-v1.json`: canonical equipment and movement records.
- `strengthos-movement-catalog-v1.schema.json`: JSON Schema for catalog validation.

Programs reference canonical movements with a stable human-readable ID such as `back-squat`, `power-clean`, or `toes-to-bar`. Session-specific prescription IDs remain separate, so the same movement can appear throughout a program without merging individual prescriptions.

## Raw URL

```text
https://raw.githubusercontent.com/OneMuppet/strengthos-movements/main/movements-v1.json
```

Clients should bundle a known-good snapshot for offline use and record the catalog revision used when authoring a program. New fields or breaking changes require a new catalog format version.

## Contributing

Movement IDs are permanent once published. Add aliases instead of renaming IDs, use equipment IDs from the catalog registry, update the revision, and validate the file before opening a pull request.

```sh
jq empty movements-v1.json
```

## License

MIT
