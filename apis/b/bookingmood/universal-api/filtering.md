# Bookingmood Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Bookingmood expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Bookingmood actions that support filtering

- [Delete Bookings](actions/delete-bookings.md)
- [Delete Calendar Events](actions/delete-calendar-events.md)
- [Delete Contacts](actions/delete-contacts.md)
- [Delete Products](actions/delete-products.md)
- [List Bookings](actions/list-bookings.md)
- [List Calendar Events](actions/list-calendar-events.md)
- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Messages](actions/list-messages.md)
- [List Payments](actions/list-payments.md)
- [List Products](actions/list-products.md)
- [List Sites](actions/list-sites.md)
- [Update Bookings](actions/update-bookings.md)
- [Update Calendar Events](actions/update-calendar-events.md)
- [Update Contacts](actions/update-contacts.md)
- [Update Payments](actions/update-payments.md)
- [Update Products](actions/update-products.md)
