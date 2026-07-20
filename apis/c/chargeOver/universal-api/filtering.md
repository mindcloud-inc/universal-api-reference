# ChargeOver Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format ChargeOver expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## ChargeOver actions that support filtering

- [List Contacts](actions/list-contacts.md)
- [List Customers](actions/list-customers.md)
- [List Invoices](actions/list-invoices.md)
- [List Items](actions/list-items.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
- [List Usage Records](actions/list-usage-records.md)
