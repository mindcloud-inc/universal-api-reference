# Flotiq Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Flotiq expects, and each action page lists the fields available to sort.

## Flotiq actions that support sorting

- [List Content Objects](actions/list-content-objects.md)
- [List Content Types](actions/list-content-types.md)
- [List Media Objects](actions/list-media-objects.md)
- [List Media Versions](actions/list-media-versions.md)
- [Search Content](actions/search-content.md)
