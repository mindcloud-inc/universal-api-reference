# Visma eAccounting Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Visma eAccounting expects, and each action page lists the fields available to sort.

## Visma eAccounting actions that support sorting

- [List Articles](actions/list-articles.md)
- [List Customer Invoice Drafts](actions/list-customer-invoice-drafts.md)
- [List Customer Invoices](actions/list-customer-invoices.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Quotes](actions/list-quotes.md)
