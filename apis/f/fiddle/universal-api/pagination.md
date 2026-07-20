# Fiddle Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Fiddle expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Fiddle actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Inventory Items](actions/list-inventory-items.md)
- [List Inventory Locations](actions/list-inventory-locations.md)
- [List Inventory Lots](actions/list-inventory-lots.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quarantined Lots](actions/list-quarantined-lots.md)
- [List Sales Order Items](actions/list-sales-order-items.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Work Orders](actions/list-work-orders.md)
