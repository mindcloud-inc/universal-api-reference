# Goody Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Goody expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-cards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Goody actions that support pagination

- [List Cards](actions/list-cards.md)
- [List Order Batch Orders](actions/list-order-batch-orders.md)
- [List Order Batch Recipients](actions/list-order-batch-recipients.md)
- [List Order Batches](actions/list-order-batches.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
