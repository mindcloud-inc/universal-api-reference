# Epicor Prophet 21 Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Epicor Prophet 21 expects, and each action page lists the fields available to sort.

## Epicor Prophet 21 actions that support sorting

- [Query Data View](actions/query-data-view.md)
- [Query Manifest Collection](actions/query-manifest-collection.md)
- [Query OData Table](actions/query-odata-table.md)
- [Query OData View](actions/query-odata-view.md)
