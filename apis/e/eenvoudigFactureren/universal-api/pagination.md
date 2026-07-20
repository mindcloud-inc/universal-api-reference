# EenvoudigFactureren Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model EenvoudigFactureren expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## EenvoudigFactureren actions that support pagination

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
