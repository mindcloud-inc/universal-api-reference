# Pling Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Pling expects, and each action page lists the fields available to sort.

## Pling actions that support sorting

- [List Content](actions/list-content.md)
- [List Content By Category](actions/list-content-by-category.md)
- [List Content By User](actions/list-content-by-user.md)
- [List Popular Content](actions/list-popular-content.md)
- [Search Content](actions/search-content.md)
