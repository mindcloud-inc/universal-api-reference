# Donorbox Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Donorbox expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Donorbox actions that support filtering

- [List Campaigns](actions/list-campaigns.md)
- [List Donations](actions/list-donations.md)
- [List Donors](actions/list-donors.md)
- [List Plans](actions/list-plans.md)
- [List Purchases](actions/list-purchases.md)
- [List Tickets](actions/list-tickets.md)
