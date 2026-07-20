# Easy Redmine Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Easy Redmine expects, and each action page lists the fields available to sort.

## Easy Redmine actions that support sorting

- [List Issues](actions/list-issues.md)
- [List Projects](actions/list-projects.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Versions](actions/list-versions.md)
