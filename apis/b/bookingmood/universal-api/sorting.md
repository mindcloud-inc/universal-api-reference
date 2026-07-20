# Bookingmood Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Bookingmood expects, and each action page lists the fields available to sort.

## Bookingmood actions that support sorting

- [List Bookings](actions/list-bookings.md)
- [List Calendar Events](actions/list-calendar-events.md)
- [List Contacts](actions/list-contacts.md)
- [List Invoices](actions/list-invoices.md)
- [List Messages](actions/list-messages.md)
- [List Payments](actions/list-payments.md)
- [List Products](actions/list-products.md)
- [List Sites](actions/list-sites.md)
