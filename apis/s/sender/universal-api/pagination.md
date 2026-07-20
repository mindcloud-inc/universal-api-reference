# Sender Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sender expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sender actions that support pagination

- [List Campaigns](actions/list-campaigns.md)
- [List Fields](actions/list-fields.md)
- [List Groups](actions/list-groups.md)
- [List Segments](actions/list-segments.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Subscribers in Group](actions/list-subscribers-in-group.md)
- [List Transactional Campaigns](actions/list-transactional-campaigns.md)
