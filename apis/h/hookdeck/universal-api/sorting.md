# Hookdeck Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Hookdeck expects, and each action page lists the fields available to sort.

## Hookdeck actions that support sorting

- [Get Connections](actions/get-connections.md)
- [Get Destinations](actions/get-destinations.md)
- [Get Events](actions/get-events.md)
- [Get Issues](actions/get-issues.md)
- [Get Requests](actions/get-requests.md)
- [Get Sources](actions/get-sources.md)
