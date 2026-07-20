# WorkflowMax Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format WorkflowMax expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## WorkflowMax actions that support filtering

- [List Clients](actions/list-clients.md)
- [List Invoices](actions/list-invoices.md)
- [List Job Costs](actions/list-job-costs.md)
- [List Job Tasks](actions/list-job-tasks.md)
- [List Jobs](actions/list-jobs.md)
- [List Payments](actions/list-payments.md)
- [List Purchase Order Bills](actions/list-purchase-order-bills.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quotes](actions/list-quotes.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Tasks](actions/list-tasks.md)
- [List Timesheets](actions/list-timesheets.md)
