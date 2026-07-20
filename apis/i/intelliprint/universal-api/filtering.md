# Intelliprint Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Intelliprint expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Intelliprint actions that support filtering

- [List Backgrounds](actions/list-backgrounds.md)
- [List Mailing List Recipients](actions/list-mailing-list-recipients.md)
- [List Mailing Lists](actions/list-mailing-lists.md)
- [List Print Jobs](actions/list-print-jobs.md)
