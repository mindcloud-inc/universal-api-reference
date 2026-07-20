# FDIC Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format FDIC expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## FDIC actions that support filtering

- [List Bank Failures](actions/list-bank-failures.md)
- [List Demographics Summary](actions/list-demographics-summary.md)
- [List Financial Institutions](actions/list-financial-institutions.md)
- [List Historical Aggregate Data](actions/list-historical-aggregate-data.md)
- [List Institution Financials](actions/list-institution-financials.md)
- [List Institution Locations](actions/list-institution-locations.md)
- [List Structure Change Events](actions/list-structure-change-events.md)
- [List Summary Of Deposits](actions/list-summary-of-deposits.md)
