# Saleshandy Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Saleshandy expects, and each action page lists the fields available to sort.

## Saleshandy actions that support sorting

- [List DNC Lists](actions/list-dnc-lists.md)
- [List Prospects](actions/list-prospects.md)
- [List Sequences](actions/list-sequences.md)
