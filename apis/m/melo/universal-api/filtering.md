# Melo Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Melo expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Melo actions that support filtering

- [List Cities](actions/list-cities.md)
- [List Departments](actions/list-departments.md)
- [List Points of Interest](actions/list-points-of-interest.md)
- [List Searches](actions/list-searches.md)
- [Search Locations](actions/search-locations.md)
