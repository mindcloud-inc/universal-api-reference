# ChargeOver Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ChargeOver expects, and each action page lists the fields available to sort.

## ChargeOver actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Customers](actions/list-customers.md)
- [List Invoices](actions/list-invoices.md)
- [List Items](actions/list-items.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
- [List Usage Records](actions/list-usage-records.md)
