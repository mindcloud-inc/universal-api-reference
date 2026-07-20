# Restdb.io Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Restdb.io expects, and each action page lists the fields available to sort.

## Restdb.io actions that support sorting

- [List Documents](actions/list-documents.md)
- [List Documents Flattened](actions/list-documents-flattened.md)
- [List Documents With Children](actions/list-documents-with-children.md)
- [List Documents With Linked References](actions/list-documents-with-linked-references.md)
- [List Documents With Media Data](actions/list-documents-with-media-data.md)
- [List Documents With Meta Fields](actions/list-documents-with-meta-fields.md)
- [List Documents With Totals](actions/list-documents-with-totals.md)
- [Search Documents](actions/search-documents.md)
