# inFlow Inventory Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model inFlow Inventory expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## inFlow Inventory actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Locations](actions/list-locations.md)
- [List Products](actions/list-products.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Stock Adjustments](actions/list-stock-adjustments.md)
- [List Stock Transfers](actions/list-stock-transfers.md)
- [List Vendors](actions/list-vendors.md)
