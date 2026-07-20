# Robopost Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Robopost expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Robopost actions that support filtering

- [List Aggregated Analytics](actions/list-aggregated-analytics.md)
- [List Social Inbox Items](actions/list-social-inbox-items.md)
- [List Social Inbox Threads Grouped by Post](actions/list-social-inbox-threads-grouped-by-post.md)
- [List Video Tasks](actions/list-video-tasks.md)
