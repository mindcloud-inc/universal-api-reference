# Sharetribe Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Sharetribe expects, and each action page lists the fields available to sort.

## Sharetribe actions that support sorting

- [Query Listings](actions/query-listings.md)
- [Query Transactions](actions/query-transactions.md)
- [Query Users](actions/query-users.md)
