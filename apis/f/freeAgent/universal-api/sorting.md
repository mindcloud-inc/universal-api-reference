# FreeAgent Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format FreeAgent expects, and each action page lists the fields available to sort.

## FreeAgent actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Projects](actions/list-projects.md)
