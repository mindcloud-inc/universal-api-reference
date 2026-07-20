# Kontent.ai Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Kontent.ai expects, and each action page lists the fields available to sort.

## Kontent.ai actions that support sorting

- [List content items](actions/list-content-items.md)
- [List content types](actions/list-content-types.md)
- [List languages](actions/list-languages.md)
- [List taxonomy groups](actions/list-taxonomy-groups.md)
