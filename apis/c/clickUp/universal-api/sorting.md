# ClickUp Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ClickUp expects, and each action page lists the fields available to sort.

## ClickUp actions that support sorting

- [List Filtered Team Tasks](actions/list-filtered-team-tasks.md)
- [List Tasks](actions/list-tasks.md)
