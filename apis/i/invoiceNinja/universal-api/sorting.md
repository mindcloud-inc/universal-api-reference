# Invoice Ninja Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Invoice Ninja expects, and each action page lists the fields available to sort.

## Invoice Ninja actions that support sorting

- [List Clients](actions/list-clients.md)
- [List Invoices](actions/list-invoices.md)
- [List Payment Terms](actions/list-payment-terms.md)
- [List Payments](actions/list-payments.md)
- [List Products](actions/list-products.md)
- [List Quotes](actions/list-quotes.md)
- [List Recurring Invoices](actions/list-recurring-invoices.md)
- [List Tax Rates](actions/list-tax-rates.md)
