# Rocketlane Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Rocketlane expects, and each action page lists the fields available to sort.

## Rocketlane actions that support sorting

- [List Comments](actions/list-comments.md)
- [List Invoices](actions/list-invoices.md)
- [List Phases](actions/list-phases.md)
- [List Projects](actions/list-projects.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Users](actions/list-users.md)
- [Search Time Entries](actions/search-time-entries.md)
