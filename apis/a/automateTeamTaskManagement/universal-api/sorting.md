# Automate Team - Task Management Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Automate Team - Task Management expects, and each action page lists the fields available to sort.

## Automate Team - Task Management actions that support sorting

- [List Categories](actions/list-categories.md)
- [List Task Users](actions/list-task-users.md)
- [List Tasks](actions/list-tasks.md)
