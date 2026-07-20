# Expiration Reminder Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Expiration Reminder expects, and each action page lists the fields available to sort.

## Expiration Reminder actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Event Logs](actions/list-event-logs.md)
- [List Expiration Items](actions/list-expiration-items.md)
- [List Locations](actions/list-locations.md)
