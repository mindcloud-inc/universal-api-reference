# Typesense Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Typesense expects, and each action page lists the fields available to sort.

## Typesense actions that support sorting

- [Natural Language Search Documents](actions/natural-language-search-documents.md)
- [Search Documents](actions/search-documents.md)
- [Vector Search Documents](actions/vector-search-documents.md)
