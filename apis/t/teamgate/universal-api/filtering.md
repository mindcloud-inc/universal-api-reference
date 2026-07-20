# Teamgate Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Teamgate expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Teamgate actions that support filtering

- [List Activities](actions/list-activities.md)
- [List Companies](actions/list-companies.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Deals](actions/list-deals.md)
- [List Lead Statuses](actions/list-lead-statuses.md)
- [List Leads](actions/list-leads.md)
- [List People](actions/list-people.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Sources](actions/list-sources.md)
- [List Users](actions/list-users.md)
- [Search Companies](actions/search-companies.md)
- [Search Deals](actions/search-deals.md)
- [Search Leads](actions/search-leads.md)
- [Search People](actions/search-people.md)
