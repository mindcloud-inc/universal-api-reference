# Content Snare Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Content Snare expects, and each action page lists the fields available to sort.

## Content Snare actions that support sorting

- [List Client Companies](actions/list-client-companies.md)
- [List Clients](actions/list-clients.md)
- [List Requests](actions/list-requests.md)
- [List Team Members](actions/list-team-members.md)
