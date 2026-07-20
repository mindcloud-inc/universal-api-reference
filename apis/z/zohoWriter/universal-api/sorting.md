# Zoho Writer Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zoho Writer expects, and each action page lists the fields available to sort.

## Zoho Writer actions that support sorting

- [List Documents](actions/list-documents.md)
- [List Fillable Templates](actions/list-fillable-templates.md)
- [List Merge Templates](actions/list-merge-templates.md)
- [List Sign Templates](actions/list-sign-templates.md)
- [List Templates](actions/list-templates.md)
