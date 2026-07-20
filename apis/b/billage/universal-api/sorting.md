# Billage Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Billage expects, and each action page lists the fields available to sort.

## Billage actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Budgets](actions/list-budgets.md)
- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Products](actions/list-products.md)
- [List Spendings](actions/list-spendings.md)
