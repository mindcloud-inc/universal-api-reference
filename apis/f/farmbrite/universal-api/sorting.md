# Farmbrite Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Farmbrite expects, and each action page lists the fields available to sort.

## Farmbrite actions that support sorting

- [List animals](actions/list-animals.md)
- [List contacts](actions/list-contacts.md)
- [List orders](actions/list-orders.md)
- [List plots](actions/list-plots.md)
- [List products](actions/list-products.md)
- [List tasks](actions/list-tasks.md)
- [List tools](actions/list-tools.md)
- [List transactions](actions/list-transactions.md)
