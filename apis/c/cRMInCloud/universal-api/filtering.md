# CRM in Cloud Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format CRM in Cloud expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## CRM in Cloud actions that support filtering

- [Search activities](actions/search-activities.md)
- [Search appointments](actions/search-appointments.md)
- [Search companies](actions/search-companies.md)
- [Search contacts](actions/search-contacts.md)
- [Search leads](actions/search-leads.md)
- [Search lists](actions/search-lists.md)
- [Search opportunities](actions/search-opportunities.md)
- [Search storage items](actions/search-storage-items.md)
