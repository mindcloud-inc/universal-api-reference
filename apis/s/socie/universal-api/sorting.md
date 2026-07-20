# Socie Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Socie expects, and each action page lists the fields available to sort.

## Socie actions that support sorting

- [List Additional Fields](actions/list-additional-fields.md)
- [List Group Memberships](actions/list-group-memberships.md)
- [List Groups](actions/list-groups.md)
- [List Members](actions/list-members.md)
