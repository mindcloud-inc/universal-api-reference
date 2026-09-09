# Walmart Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Walmart expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-feed-item-status?connectionId=$CONNECTION_ID&limit=25&offset=0&feedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Walmart actions that support pagination

- [Get Feed Item Status](actions/get-feed-item-status.md)
- [Get Inbound Shipment Errors](actions/get-inbound-shipment-errors.md)
- [Get Inbound Shipment Items](actions/get-inbound-shipment-items.md)
- [List Feed Statuses](actions/list-feed-statuses.md)
- [List Inbound Shipments](actions/list-inbound-shipments.md)
- [List Inventory Levels](actions/list-inventory-levels.md)
- [List Released Orders](actions/list-released-orders.md)
- [List Returns](actions/list-returns.md)
- [Recon Report](actions/recon-report.md)
