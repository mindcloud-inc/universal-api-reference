# Iris Dfir Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Iris Dfir expects, and each action page lists the fields available to sort.

## Iris Dfir actions that support sorting

- [List Alerts](actions/list-alerts.md)
- [List Alerts Legacy](actions/list-alerts-legacy.md)
- [List Assets](actions/list-assets.md)
- [List Cases](actions/list-cases.md)
- [List Note Directories](actions/list-note-directories.md)
- [List Tasks](actions/list-tasks.md)
