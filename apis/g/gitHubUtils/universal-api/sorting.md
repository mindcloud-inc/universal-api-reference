# GitHub Utils Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format GitHub Utils expects, and each action page lists the fields available to sort.

## GitHub Utils actions that support sorting

- [List Authenticated User Repositories](actions/list-authenticated-user-repositories.md)
- [List Pull Requests](actions/list-pull-requests.md)
- [List Repository Issues](actions/list-repository-issues.md)
- [Search Issues and Pull Requests](actions/search-issues-and-pull-requests.md)
- [Search Repositories](actions/search-repositories.md)
