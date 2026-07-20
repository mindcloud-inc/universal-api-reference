# GSA Public Comment Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format GSA Public Comment expects, and each action page lists the fields available to sort.

## GSA Public Comment actions that support sorting

- [List Comments](actions/list-comments.md)
- [List Dockets](actions/list-dockets.md)
- [List Documents](actions/list-documents.md)
