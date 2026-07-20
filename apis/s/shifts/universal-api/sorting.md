# 7shifts Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format 7shifts expects, and each action page lists the fields available to sort.

## 7shifts actions that support sorting

- [List Shifts](actions/list-shifts.md)
- [List Time Punches](actions/list-time-punches.md)
- [List Users](actions/list-users.md)
