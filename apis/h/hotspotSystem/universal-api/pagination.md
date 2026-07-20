# HotspotSystem Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model HotspotSystem expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## HotspotSystem actions that support pagination

- [List Customers](actions/list-customers.md)
- [List Customers by Location](actions/list-customers-by-location.md)
- [List Locations](actions/list-locations.md)
- [List MAC Transactions](actions/list-mac-transactions.md)
- [List MAC Transactions by Location](actions/list-mac-transactions-by-location.md)
- [List Paid Transactions](actions/list-paid-transactions.md)
- [List Social Transactions](actions/list-social-transactions.md)
- [List Social Transactions by Location](actions/list-social-transactions-by-location.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Subscribers by Location](actions/list-subscribers-by-location.md)
- [List Voucher Transactions](actions/list-voucher-transactions.md)
- [List Voucher Transactions by Location](actions/list-voucher-transactions-by-location.md)
