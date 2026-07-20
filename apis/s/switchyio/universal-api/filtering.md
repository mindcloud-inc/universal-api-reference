# Switchy.io Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Switchy.io expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Switchy.io actions that support filtering

- [List Domains](actions/list-domains.md)
- [List Folders](actions/list-folders.md)
- [List Link Scripts](actions/list-link-scripts.md)
- [List Links](actions/list-links.md)
- [List Pixels](actions/list-pixels.md)
- [List Tokens](actions/list-tokens.md)
- [List UTM Templates](actions/list-utm-templates.md)
