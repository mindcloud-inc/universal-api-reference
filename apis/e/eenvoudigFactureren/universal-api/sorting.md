# EenvoudigFactureren Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format EenvoudigFactureren expects, and each action page lists the fields available to sort.

## EenvoudigFactureren actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Client Contacts](actions/list-client-contacts.md)
- [List Clients](actions/list-clients.md)
- [List Custom Documents](actions/list-custom-documents.md)
- [List Deliveries](actions/list-deliveries.md)
- [List Invoice Items](actions/list-invoice-items.md)
- [List Invoice Payments](actions/list-invoice-payments.md)
- [List Invoice Remarks](actions/list-invoice-remarks.md)
- [List Invoices](actions/list-invoices.md)
- [List Order Items](actions/list-order-items.md)
- [List Orders](actions/list-orders.md)
- [List Payment Requests](actions/list-payment-requests.md)
- [List Projects](actions/list-projects.md)
- [List Purchases](actions/list-purchases.md)
- [List Quote Items](actions/list-quote-items.md)
- [List Quotes](actions/list-quotes.md)
- [List Receipts](actions/list-receipts.md)
- [List Stock Items](actions/list-stock-items.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Suppliers](actions/list-suppliers.md)
