# STEL Order Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model STEL Order expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-account-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## STEL Order actions that support pagination

- [List Account Categories](actions/list-account-categories.md)
- [List Addresses](actions/list-addresses.md)
- [List Bank Accounts](actions/list-bank-accounts.md)
- [List Calendars](actions/list-calendars.md)
- [List Clients](actions/list-clients.md)
- [List Contacts](actions/list-contacts.md)
- [List Delivery Options](actions/list-delivery-options.md)
- [List Document States](actions/list-document-states.md)
- [List Event Types](actions/list-event-types.md)
- [List Events](actions/list-events.md)
- [List Expense Categories](actions/list-expense-categories.md)
- [List Expense States](actions/list-expense-states.md)
- [List Expenses](actions/list-expenses.md)
- [List Item Images](actions/list-item-images.md)
- [List Item Rates](actions/list-item-rates.md)
- [List Ordinary Invoice Receipts](actions/list-ordinary-invoice-receipts.md)
- [List Ordinary Invoices](actions/list-ordinary-invoices.md)
- [List Payment Options](actions/list-payment-options.md)
- [List Payment Terms](actions/list-payment-terms.md)
- [List Potential Clients](actions/list-potential-clients.md)
- [List Product Categories](actions/list-product-categories.md)
- [List Product Components](actions/list-product-components.md)
- [List Product Warehouses](actions/list-product-warehouses.md)
- [List Products](actions/list-products.md)
- [List Refund Invoice Receipts](actions/list-refund-invoice-receipts.md)
- [List Refund Invoices](actions/list-refund-invoices.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Services](actions/list-services.md)
- [List Work Orders](actions/list-work-orders.md)
