# StrengthOS Movement Catalog

The public, versioned movement and equipment vocabulary used by StrengthOS.

## Files

- `movements-v2.json`: current canonical catalog with equipment alternatives, compound reporting profiles, difficulty, movement families, coaching content, relationships, and lifecycle status.
- `strengthos-movement-catalog-v2.schema.json`: JSON Schema for the current catalog.
- `movements-v1.json`: frozen legacy catalog for existing clients.
- `strengthos-movement-catalog-v1.schema.json`: legacy catalog schema.

Programs reference canonical movements with a stable human-readable ID such as `back-squat`, `power-clean`, or `toes-to-bar`. Session-specific prescription IDs remain separate, so the same movement can appear throughout a program without merging individual prescriptions.

## Raw URL

```text
https://raw.githubusercontent.com/OneMuppet/strengthos-movements/main/movements-v2.json
```

Clients should bundle a known-good snapshot for offline use and record the catalog revision used when authoring a program. New fields or breaking changes require a new catalog format version.

## Contributing

Movement IDs are permanent once published. External exercise databases may inform research, but every record must be authored and reviewed against the native StrengthOS schema. Add aliases instead of renaming IDs, define complete equipment alternatives, update the revision, and validate the file before opening a pull request.

```sh
npx --yes ajv-cli@5 validate --spec=draft2020 \
  -s strengthos-movement-catalog-v2.schema.json \
  -d movements-v2.json
```

## License

MIT
