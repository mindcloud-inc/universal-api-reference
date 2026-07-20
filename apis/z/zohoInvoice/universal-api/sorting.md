# Zoho Invoice Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zoho Invoice expects, and each action page lists the fields available to sort.

## Zoho Invoice actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Customer Payments](actions/list-customer-payments.md)
- [List Expenses](actions/list-expenses.md)
- [List Invoices](actions/list-invoices.md)
- [List Items](actions/list-items.md)
