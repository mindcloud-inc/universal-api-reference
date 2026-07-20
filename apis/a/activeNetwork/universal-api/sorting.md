# Active Network Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Active Network expects, and each action page lists the fields available to sort.

## Active Network actions that support sorting

- [Search Assets](actions/search-assets.md)
- [Search Kids Assets](actions/search-kids-assets.md)
