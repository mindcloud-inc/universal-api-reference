# Housecall Pro Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Housecall Pro expects, and each action page lists the fields available to sort.

## Housecall Pro actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Employees](actions/list-employees.md)
- [List Estimates](actions/list-estimates.md)
- [List Invoices](actions/list-invoices.md)
- [List Jobs](actions/list-jobs.md)
- [List Leads](actions/list-leads.md)
