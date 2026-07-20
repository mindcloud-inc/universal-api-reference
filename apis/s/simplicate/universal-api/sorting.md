# Simplicate Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Simplicate expects, and each action page lists the fields available to sort.

## Simplicate actions that support sorting

- [List Employees](actions/list-employees.md)
- [List Hours](actions/list-hours.md)
- [List Invoices](actions/list-invoices.md)
- [List Organizations](actions/list-organizations.md)
- [List Payments](actions/list-payments.md)
- [List Services](actions/list-services.md)
