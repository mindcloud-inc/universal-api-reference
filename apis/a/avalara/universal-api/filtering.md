# Avalara AvaTax Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Avalara AvaTax expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Avalara AvaTax actions that support filtering

- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Entity Use Codes](actions/list-entity-use-codes.md)
- [List Items By Company](actions/list-items-by-company.md)
- [List Jurisdictions Hierarchy](actions/list-jurisdictions-hierarchy.md)
- [List Nexus By Company](actions/list-nexus-by-company.md)
- [List Parameters](actions/list-parameters.md)
- [List Tax Authority Types](actions/list-tax-authority-types.md)
- [List Tax Codes By Company](actions/list-tax-codes-by-company.md)
- [List Tax Rules](actions/list-tax-rules.md)
- [List Transactions By Company](actions/list-transactions-by-company.md)
- [Query Companies](actions/query-companies.md)
- [Query Customers](actions/query-customers.md)
- [Query Tax Codes](actions/query-tax-codes.md)
