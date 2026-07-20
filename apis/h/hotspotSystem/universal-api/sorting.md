# HotspotSystem Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format HotspotSystem expects, and each action page lists the fields available to sort.

## HotspotSystem actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Customers by Location](actions/list-customers-by-location.md)
- [List Locations](actions/list-locations.md)
- [List MAC Transactions](actions/list-mac-transactions.md)
- [List MAC Transactions by Location](actions/list-mac-transactions-by-location.md)
- [List Paid Transactions](actions/list-paid-transactions.md)
- [List Social Transactions](actions/list-social-transactions.md)
- [List Social Transactions by Location](actions/list-social-transactions-by-location.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Subscribers by Location](actions/list-subscribers-by-location.md)
- [List Voucher Transactions](actions/list-voucher-transactions.md)
- [List Voucher Transactions by Location](actions/list-voucher-transactions-by-location.md)
