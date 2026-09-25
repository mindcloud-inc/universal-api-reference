# Microsoft Entra Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Microsoft Entra expects, and each action page lists the fields available to sort.

## Microsoft Entra actions that support sorting

- [List Group Transitive Memberships](actions/list-group-transitive-memberships.md)
- [List Groups](actions/list-groups.md)
- [List User Memberships](actions/list-user-memberships.md)
- [List User Transitive Memberships](actions/list-user-transitive-memberships.md)
- [List Users](actions/list-users.md)
