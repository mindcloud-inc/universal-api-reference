# Qlik Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Qlik expects, and each action page lists the fields available to sort.

## Qlik actions that support sorting

- [Filter Groups](actions/filter-groups.md)
- [Filter Users](actions/filter-users.md)
- [List Collection Items](actions/list-collection-items.md)
- [List Collections](actions/list-collections.md)
- [List Groups](actions/list-groups.md)
- [List Item Collections](actions/list-item-collections.md)
- [List Items](actions/list-items.md)
- [List Published Items](actions/list-published-items.md)
- [List Reloads](actions/list-reloads.md)
- [List Spaces](actions/list-spaces.md)
- [List Users](actions/list-users.md)
