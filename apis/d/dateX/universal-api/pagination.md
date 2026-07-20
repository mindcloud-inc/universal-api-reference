# DateX (Legacy) Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DateX (Legacy) expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-available-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0&warehouse=string&filters.project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DateX (Legacy) actions that support pagination

- [List Available Inventory](actions/list-available-inventory.md)
- [List Inventory](actions/list-inventory.md)
- [List Owners](actions/list-owners.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Sales Shipments](actions/list-sales-shipments.md)
- [List Shipping Details](actions/list-shipping-details.md)
- [List Warehouses](actions/list-warehouses.md)
