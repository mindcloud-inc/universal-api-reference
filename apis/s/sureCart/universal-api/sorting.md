# SureCart Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format SureCart expects, and each action page lists the fields available to sort.

## SureCart actions that support sorting

- [List Checkouts](actions/list-checkouts.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Prices](actions/list-prices.md)
- [List Products](actions/list-products.md)
- [List Purchases](actions/list-purchases.md)
- [List Refunds](actions/list-refunds.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Webhook Endpoints](actions/list-webhook-endpoints.md)
