# LimoExpress Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format LimoExpress expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## LimoExpress actions that support filtering

- [Get Pricing](actions/get-pricing.md)
- [List All Currencies](actions/list-all-currencies.md)
- [List Booking Offers](actions/list-booking-offers.md)
- [List Bookings](actions/list-bookings.md)
- [List Clients](actions/list-clients.md)
- [List Countries](actions/list-countries.md)
- [List Expenses](actions/list-expenses.md)
- [List Invoices](actions/list-invoices.md)
- [List Passengers](actions/list-passengers.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Users](actions/list-users.md)
- [List Vehicle Classes](actions/list-vehicle-classes.md)
- [List Vehicles](actions/list-vehicles.md)
