# Rossum Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Rossum expects, and each action page lists the fields available to sort.

## Rossum actions that support sorting

- [List Documents](actions/list-documents.md)
- [List Emails](actions/list-emails.md)
- [List Schemas](actions/list-schemas.md)
- [List Workspaces](actions/list-workspaces.md)
