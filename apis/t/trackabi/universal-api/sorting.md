# Trackabi Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Trackabi expects, and each action page lists the fields available to sort.

## Trackabi actions that support sorting

- [List Clients](actions/list-clients.md)
- [List Leaves](actions/list-leaves.md)
- [List Members](actions/list-members.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Task Subtasks](actions/list-task-subtasks.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
