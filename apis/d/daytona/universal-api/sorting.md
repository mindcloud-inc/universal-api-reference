# Daytona Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Daytona expects, and each action page lists the fields available to sort.

## Daytona actions that support sorting

- [List Sandboxes Paginated](actions/list-sandboxes-paginated.md)
- [List Snapshots](actions/list-snapshots.md)
