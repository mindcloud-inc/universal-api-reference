# Harbour Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Harbour expects, and each action page lists the fields available to sort.

## Harbour actions that support sorting

- [List Agreement Links](actions/list-agreement-links.md)
- [List Agreements](actions/list-agreements.md)
- [List Brands](actions/list-brands.md)
- [List Documents](actions/list-documents.md)
- [List Folders](actions/list-folders.md)
- [List Items](actions/list-items.md)
- [List Organizations](actions/list-organizations.md)
