# uaro-loot-ledger

A single-file, no-build web app for calculating expected zeny per hour on a uaRO (Ragnarok Online) farming run. Add every monster you're killing, their drop tables, and their kill rates, and it tallies the total expected value for the whole spot.

## Features

- **Multi-monster runs** — add any number of monsters to a single run, each with its own kills/hour and drop table.
- **Per-monster and total EV** — see each monster's zeny/hour subtotal plus the combined total for the whole run.
- **Comma-formatted zeny values** — enter `1000000`, it displays as `1,000,000 z`.
- **Item ID + quick actions** — add an optional item ID per item to:
  - **Copy** an `@ws <id>` command to the clipboard.
  - **Open on RateMyServer** (`RMS ↗`) to look up the item.
- **Save, load, and adjust runs** — name a run and save it; reload it later to tweak drop rates or zeny values as prices shift, then save over it or as a new run.
- **Import / export** — back up all saved runs to a JSON file, or import one to merge runs back in (e.g. moving between browsers/devices).
- **Local, private storage** — saved runs live in your browser's `localStorage`. Nothing is sent anywhere.

## Usage

1. Open `loot-ledger.html` in any modern browser — no server, build step, or install required.
2. Add a monster, set its kills/hour, and fill in its drop table (item name, drop chance %, zeny value).
3. Add more monsters as needed; the total EV/hour updates live.
4. Name the run and click **Save run** to keep it. Use **Load & adjust** on a saved run to edit and update it later.
5. Use **Export** / **Import** to back up or transfer your saved runs between browsers.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no framework, no dependencies, no build tooling. Fonts (Fraunces, Inter) are loaded from Google Fonts; everything else is self-contained in the one file.

## File structure

```
loot-ledger.html   # the entire app
```

## Notes

- Saved runs are stored per-browser via `localStorage`; clearing site data or switching browsers loses them unless you've exported first.
- The RMS link opens `ratemyserver.net`'s item page in a new tab — it does not pull data back into the app (cross-origin browser restrictions prevent that).

## License

Use, modify, and share freely.
