# Locu Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Locu expects, and each action page lists the fields available to sort.

## Locu actions that support sorting

- [List Activities](actions/list-activities.md)
- [List Projects](actions/list-projects.md)
- [List Sessions](actions/list-sessions.md)
- [List Tasks](actions/list-tasks.md)
