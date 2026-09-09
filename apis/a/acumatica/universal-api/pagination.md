# Acumatica Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Acumatica expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-orders-list?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Acumatica actions that support pagination

- [List Purchase Orders](actions/get-purchase-orders-list.md)
- [List Purchase Receipts](actions/get-purchase-receipt.md)
- [List Bills](actions/list-bills.md)
- [List Contacts](actions/list-contacts.md)
- [List Customers](actions/list-customers.md)
- [List Invoices](actions/list-invoices.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Payments](actions/list-payments.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Shipments](actions/list-shipments.md)
- [List Vendors](actions/list-vendors.md)
- [List Stock Items](actions/retrieve-stock-item.md)
- [Search By Entity](actions/search-by-entity.md)
- [Search By Generic Inquiry](actions/search-by-generic-inquiry.md)
