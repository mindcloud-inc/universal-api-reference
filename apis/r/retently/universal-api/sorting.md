# Retently Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Retently expects, and each action page lists the fields available to sort.

## Retently actions that support sorting

- [List Companies](actions/list-companies.md)
- [List Customers](actions/list-customers.md)
- [List Feedback](actions/list-feedback.md)
- [List Outbox](actions/list-outbox.md)
