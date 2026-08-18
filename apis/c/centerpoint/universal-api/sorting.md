# Centerpoint Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Centerpoint expects, and each action page lists the fields available to sort.

## Centerpoint actions that support sorting

- [Get Invoice](actions/get-invoice.md)
- [List Companies](actions/list-companies.md)
- [List Model Files](actions/list-model-files.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Properties](actions/list-properties.md)
