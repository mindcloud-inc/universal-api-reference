# Crowdin Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Crowdin expects, and each action page lists the fields available to sort.

## Crowdin actions that support sorting

- [List Branches](actions/list-branches.md)
- [List Directories](actions/list-directories.md)
- [List Files](actions/list-files.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
