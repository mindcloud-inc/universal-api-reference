# SureCart Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SureCart expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-checkouts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SureCart actions that support pagination

- [List Checkouts](actions/list-checkouts.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Prices](actions/list-prices.md)
- [List Products](actions/list-products.md)
- [List Purchases](actions/list-purchases.md)
- [List Refunds](actions/list-refunds.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Webhook Endpoints](actions/list-webhook-endpoints.md)
