# Recurly Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Recurly expects, and each action page lists the fields available to sort.

## Recurly actions that support sorting

- [List Account Subscriptions](actions/list-account-subscriptions.md)
- [List Accounts](actions/list-accounts.md)
- [List Invoices](actions/list-invoices.md)
- [List Plans](actions/list-plans.md)
- [List Sites](actions/list-sites.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
