# Sumo Logic Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Sumo Logic expects, and each action page lists the fields available to sort.

## Sumo Logic actions that support sorting

- [List Roles](actions/list-roles.md)
- [List Roles V2](actions/list-roles-v2.md)
- [List Users](actions/list-users.md)
