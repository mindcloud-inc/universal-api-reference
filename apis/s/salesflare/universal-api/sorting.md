# Salesflare Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Salesflare expects, and each action page lists the fields available to sort.

## Salesflare actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Contacts](actions/list-contacts.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Stages](actions/list-stages.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
