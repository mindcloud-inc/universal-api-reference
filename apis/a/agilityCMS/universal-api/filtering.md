# Agility CMS Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Agility CMS expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Agility CMS actions that support filtering

- [List Categories (Fetch)](actions/list-categories-fetch.md)
- [List Categories (Preview)](actions/list-categories-preview.md)
- [List Content Items (Fetch)](actions/list-content-items-fetch.md)
- [List Content Items (Preview)](actions/list-content-items-preview.md)
- [List Content Items V1 (Fetch)](actions/list-content-items-v1-fetch.md)
- [List Content Items V1 (Preview)](actions/list-content-items-v1-preview.md)
- [List Posts (Fetch)](actions/list-posts-fetch.md)
- [List Posts (Preview)](actions/list-posts-preview.md)
