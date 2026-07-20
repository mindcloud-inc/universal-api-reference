# DivvyHQ Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format DivvyHQ expects, and each action page lists the fields available to sort.

## DivvyHQ actions that support sorting

- [List Campaigns](actions/list-campaigns.md)
- [List Content Items](actions/list-content-items.md)
- [List Production Tasks](actions/list-production-tasks.md)
