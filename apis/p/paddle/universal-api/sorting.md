# Paddle Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Paddle expects, and each action page lists the fields available to sort.

## Paddle actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Discounts](actions/list-discounts.md)
- [List Notification Settings](actions/list-notification-settings.md)
- [List Notifications](actions/list-notifications.md)
- [List Prices](actions/list-prices.md)
- [List Products](actions/list-products.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
