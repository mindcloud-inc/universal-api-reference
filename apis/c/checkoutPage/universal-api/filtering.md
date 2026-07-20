# Checkout Page Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Checkout Page expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Checkout Page actions that support filtering

- [List Bookings](actions/list-bookings.md)
- [List Checkout Pages](actions/list-checkout-pages.md)
- [List Coupons](actions/list-coupons.md)
- [List Customers](actions/list-customers.md)
- [List Events](actions/list-events.md)
- [List Forms](actions/list-forms.md)
- [List Payments](actions/list-payments.md)
- [List Subscriptions](actions/list-subscriptions.md)
