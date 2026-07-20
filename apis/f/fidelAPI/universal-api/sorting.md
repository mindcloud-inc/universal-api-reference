# Fidel API Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Fidel API expects, and each action page lists the fields available to sort.

## Fidel API actions that support sorting

- [List Brands](actions/list-brands.md)
- [List Cards](actions/list-cards.md)
- [List Locations](actions/list-locations.md)
- [List Locations by Brand](actions/list-locations-by-brand.md)
- [List MID Requests](actions/list-mid-requests.md)
- [List MIDs](actions/list-mids.md)
- [List Missing Transaction Requests](actions/list-missing-transaction-requests.md)
- [List Offers](actions/list-offers.md)
- [List Programs](actions/list-programs.md)
- [List Transactions by Card](actions/list-transactions-by-card.md)
- [List Transactions by Program](actions/list-transactions-by-program.md)
