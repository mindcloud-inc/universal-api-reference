# Anabix CRM Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Anabix CRM expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Anabix CRM actions that support filtering

- [List Activities](actions/list-activities.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Lists](actions/list-lists.md)
- [List Organizations](actions/list-organizations.md)
- [List Tasks](actions/list-tasks.md)
