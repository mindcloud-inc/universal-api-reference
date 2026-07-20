# WorkflowMax Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format WorkflowMax expects, and each action page lists the fields available to sort.

## WorkflowMax actions that support sorting

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
