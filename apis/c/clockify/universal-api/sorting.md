# Clockify Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Clockify expects, and each action page lists the fields available to sort.

## Clockify actions that support sorting

- [List Project Tasks](actions/list-project-tasks.md)
- [List Workspace Clients](actions/list-workspace-clients.md)
- [List Workspace Projects](actions/list-workspace-projects.md)
- [List Workspace Tags](actions/list-workspace-tags.md)
- [List Workspace Users](actions/list-workspace-users.md)
- [Search Workspace Users](actions/search-workspace-users.md)
