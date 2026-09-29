# Baltimore Homicide Data Fetcher (Go)

A containerized Go command-line tool that retrieves annual Baltimore City homicide tables, extracts victim ages, and reports yearly totals and counts for victims age 18 or younger.

## Highlights

- Fetches 2020–2025 source pages with timeouts and alternate URL fallbacks.
- Parses tabular HTML using the standard library—no third-party dependencies.
- Prints results to the terminal or writes structured CSV/JSON output.
- Ships as a small multi-stage Docker image.

## Run

```bash
go run .
go run . --output json
```

For Docker, run `./run.sh` or `./run.sh --output csv`. Generated files are written to `out/`.

The source site’s HTML can change; empty results should be treated as a source or schema issue rather than a zero-count result.
