# Intradesk Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Intradesk expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Intradesk actions that support filtering

- [List Assets](actions/list-assets.md)
- [List Clients](actions/list-clients.md)
- [List Dashboard Tickets](actions/list-dashboard-tickets.md)
- [List Employees](actions/list-employees.md)
- [List Knowledge Base Articles](actions/list-knowledge-base-articles.md)
- [List Tasks](actions/list-tasks.md)
