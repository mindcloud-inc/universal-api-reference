# imgix Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format imgix expects, and each action page lists the fields available to sort.

## imgix actions that support sorting

- [List Assets](actions/list-assets.md)
- [List Reports](actions/list-reports.md)
- [List Sources](actions/list-sources.md)
