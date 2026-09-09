Monthly distinct buyer and seller wallet sets.

Each `YYYY-MM.json`:

```json
{"month":"YYYY-MM","buyers":["tz1..."],"sellers":["tz1..."]}
```

Arrays are sorted unique addresses from paid objkt-indexed sales in that month.
Yearly unions live in `data/backfill/years.json`.
