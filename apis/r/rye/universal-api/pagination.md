# Rye Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rye expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/list-checkout-intent-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rye actions that support pagination

- [List Checkout Intent Shipments](actions/list-checkout-intent-shipments.md)
- [List Checkout Intents](actions/list-checkout-intents.md)
- [List Shipments](actions/list-shipments.md)
- [List Transactions](actions/list-transactions.md)
