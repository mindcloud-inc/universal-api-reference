# Coda Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Coda expects, and each action page lists the fields available to sort.

## Coda actions that support sorting

- [List Controls](actions/list-controls.md)
- [List Formulas](actions/list-formulas.md)
- [List Rows](actions/list-rows.md)
- [List Tables](actions/list-tables.md)
