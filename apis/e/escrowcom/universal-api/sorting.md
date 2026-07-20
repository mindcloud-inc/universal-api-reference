# Escrow.com Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Escrow.com expects, and each action page lists the fields available to sort.

## Escrow.com actions that support sorting

- [List Partner Customers](actions/list-partner-customers.md)
- [List Partner Transactions](actions/list-partner-transactions.md)
- [List Transactions](actions/list-transactions.md)
