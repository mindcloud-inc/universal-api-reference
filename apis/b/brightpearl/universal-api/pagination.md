# Brightpearl Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Brightpearl expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Brightpearl actions that support pagination

- [List Goods-In Notes](actions/list-goods-in-notes.md)
- [List Goods-Out Notes](actions/list-goods-out-notes.md)
- [List Orders](actions/list-orders.md)
