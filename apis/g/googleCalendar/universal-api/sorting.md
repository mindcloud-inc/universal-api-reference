# Google Calendar Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Google Calendar expects, and each action page lists the fields available to sort.

## Google Calendar actions that support sorting

- [List Events](actions/list-events.md)
