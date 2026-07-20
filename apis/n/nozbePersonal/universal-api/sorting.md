# Nozbe Personal Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Nozbe Personal expects, and each action page lists the fields available to sort.

## Nozbe Personal actions that support sorting

- [List Reminders](actions/list-reminders.md)
- [List Tag Assignments](actions/list-tag-assignments.md)
- [List Task Recurrences](actions/list-task-recurrences.md)
- [List Teams](actions/list-teams.md)
