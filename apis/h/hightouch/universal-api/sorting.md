# Hightouch Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Hightouch expects, and each action page lists the fields available to sort.

## Hightouch actions that support sorting

- [List Destinations](actions/list-destinations.md)
- [List Event Contracts](actions/list-event-contracts.md)
- [List IDR Runs](actions/list-idr-runs.md)
- [List Models](actions/list-models.md)
- [List Sources](actions/list-sources.md)
- [List Sync Runs](actions/list-sync-runs.md)
- [List Syncs](actions/list-syncs.md)
