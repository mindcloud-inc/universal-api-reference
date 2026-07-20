# Salesrobot Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Salesrobot expects, and each action page lists the fields available to sort.

## Salesrobot actions that support sorting

- [List Campaign Prospects](actions/list-campaign-prospects.md)
- [List LinkedIn Accounts](actions/list-linked-in-accounts.md)
