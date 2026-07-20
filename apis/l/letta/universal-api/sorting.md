# Letta Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Letta expects, and each action page lists the fields available to sort.

## Letta actions that support sorting

- [List Agents](actions/list-agents.md)
