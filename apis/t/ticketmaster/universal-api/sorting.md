# Ticketmaster Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Ticketmaster expects, and each action page lists the fields available to sort.

## Ticketmaster actions that support sorting

- [List Attractions](actions/list-attractions.md)
- [List Classifications](actions/list-classifications.md)
- [List Events](actions/list-events.md)
- [List Venues](actions/list-venues.md)
