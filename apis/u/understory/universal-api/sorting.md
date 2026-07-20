# Understory Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Understory expects, and each action page lists the fields available to sort.

## Understory actions that support sorting

- [List Bookings](actions/list-bookings.md)
- [List Orders](actions/list-orders.md)
