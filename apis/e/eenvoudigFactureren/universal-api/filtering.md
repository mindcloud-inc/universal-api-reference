# EenvoudigFactureren Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format EenvoudigFactureren expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## EenvoudigFactureren actions that support filtering

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
