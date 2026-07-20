# Hookdeck Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Hookdeck expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Hookdeck actions that support filtering

- [Get Connections](actions/get-connections.md)
- [Get Destinations](actions/get-destinations.md)
- [Get Events](actions/get-events.md)
- [Get Issues](actions/get-issues.md)
- [Get Requests](actions/get-requests.md)
- [Get Sources](actions/get-sources.md)
