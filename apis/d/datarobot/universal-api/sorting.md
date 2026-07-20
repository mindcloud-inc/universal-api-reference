# Datarobot Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Datarobot expects, and each action page lists the fields available to sort.

## Datarobot actions that support sorting

- [List Datasets](actions/list-datasets.md)
- [List Deployments](actions/list-deployments.md)
- [List Projects](actions/list-projects.md)
- [List Use Cases](actions/list-use-cases.md)
