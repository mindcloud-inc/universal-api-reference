# Intradesk Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Intradesk expects, and each action page lists the fields available to sort.

## Intradesk actions that support sorting

- [List Assets](actions/list-assets.md)
- [List Clients](actions/list-clients.md)
- [List Dashboard Tickets](actions/list-dashboard-tickets.md)
- [List Employees](actions/list-employees.md)
- [List Knowledge Base Articles](actions/list-knowledge-base-articles.md)
- [List Tasks](actions/list-tasks.md)
