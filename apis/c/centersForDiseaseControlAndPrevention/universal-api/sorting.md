# Centers for Disease Control and Prevention Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Centers for Disease Control and Prevention expects, and each action page lists the fields available to sort.

## Centers for Disease Control and Prevention actions that support sorting

- [Search Media](actions/search-media.md)
