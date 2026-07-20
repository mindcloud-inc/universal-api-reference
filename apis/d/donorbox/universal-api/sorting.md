# Donorbox Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Donorbox expects, and each action page lists the fields available to sort.

## Donorbox actions that support sorting

- [List Campaigns](actions/list-campaigns.md)
- [List Donations](actions/list-donations.md)
- [List Donors](actions/list-donors.md)
- [List Events](actions/list-events.md)
- [List Plans](actions/list-plans.md)
- [List Purchases](actions/list-purchases.md)
- [List Tickets](actions/list-tickets.md)
