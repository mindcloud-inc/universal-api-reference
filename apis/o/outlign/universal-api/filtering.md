# Outlign Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Outlign expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Outlign actions that support filtering

- [List Clients By Company](actions/list-clients-by-company.md)
- [List Projects By Client](actions/list-projects-by-client.md)
- [List Projects By Company](actions/list-projects-by-company.md)
- [Search Clients By Title](actions/search-clients-by-title.md)
- [Search Projects By Title](actions/search-projects-by-title.md)
