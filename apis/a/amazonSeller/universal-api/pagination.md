# Amazon Seller Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Amazon Seller expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-labels?connectionId=$CONNECTION_ID&limit=25&offset=0&shipmentId=string&pageType=string&labelType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Amazon Seller actions that support pagination

- [Get Labels](actions/get-labels.md)
- [Get Marketplace Participations](actions/get-marketplace-participations.md)
- [Get Order Metrics](actions/get-order-metrics.md)
- [List Financial Events by Order ID](actions/list-financial-events-by-order-id.md)
- [List Inbound Plans](actions/list-inbound-plans.md)
- [List Settlement Report List](actions/list-settlement-report-list.md)
- [Search Listings Items](actions/search-listings-items.md)
- [Search Orders](actions/search-orders-v2026.md)
