# SOS Inventory Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SOS Inventory expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-adjustments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SOS Inventory actions that support pagination

- [List Adjustments](actions/list-adjustments.md)
- [List Builds](actions/list-builds.md)
- [List Customers](actions/list-customers.md)
- [List Estimates](actions/list-estimates.md)
- [List Invoices](actions/list-invoices.md)
- [List Item Receipts](actions/list-item-receipts.md)
- [List Items](actions/list-items.md)
- [List Locations](actions/list-locations.md)
- [List Lots](actions/list-lots.md)
- [List Pick Tickets](actions/list-pick-tickets.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Returns](actions/list-returns.md)
- [List Returns to Vendors](actions/list-returns-to-vendors.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Sales Receipts](actions/list-sales-receipts.md)
- [List Shipments](actions/list-shipments.md)
- [List Transfers](actions/list-transfers.md)
- [List Vendors](actions/list-vendors.md)
- [List Work Orders](actions/list-work-orders.md)
