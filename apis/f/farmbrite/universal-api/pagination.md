# Farmbrite Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Farmbrite expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-animals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Farmbrite actions that support pagination

- [List animals](actions/list-animals.md)
- [List contacts](actions/list-contacts.md)
- [List orders](actions/list-orders.md)
- [List plots](actions/list-plots.md)
- [List products](actions/list-products.md)
- [List tasks](actions/list-tasks.md)
- [List tools](actions/list-tools.md)
- [List transactions](actions/list-transactions.md)
