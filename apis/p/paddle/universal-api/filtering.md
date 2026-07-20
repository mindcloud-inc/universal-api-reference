# Paddle Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Paddle expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Paddle actions that support filtering

- [List Customers](actions/list-customers.md)
- [List Discounts](actions/list-discounts.md)
- [List Notification Settings](actions/list-notification-settings.md)
- [List Notifications](actions/list-notifications.md)
- [List Prices](actions/list-prices.md)
- [List Products](actions/list-products.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Transactions](actions/list-transactions.md)
