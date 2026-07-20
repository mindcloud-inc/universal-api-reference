# Priority Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Priority expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Priority actions that support filtering

- [List AP Invoices](actions/list-ap-invoices.md)
- [List AR Invoices](actions/list-ar-invoices.md)
- [List Banks](actions/list-banks.md)
- [List Companies](actions/list-companies.md)
- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Customer Documents](actions/list-customer-documents.md)
- [List Customers](actions/list-customers.md)
- [List Document Types](actions/list-document-types.md)
- [List Part Balances](actions/list-part-balances.md)
- [List Parts](actions/list-parts.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quotation Documents](actions/list-quotation-documents.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Shippers](actions/list-shippers.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Users](actions/list-users.md)
- [List Warehouses](actions/list-warehouses.md)
