# Mighty Networks Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mighty Networks expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&networkId=%7B%7Bcredentials.networkId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mighty Networks actions that support pagination

- [List Events](actions/list-events.md)
- [List Network Members](actions/list-network-members.md)
- [List Plans](actions/list-plans.md)
- [List Post Comments](actions/list-post-comments.md)
- [List Posts](actions/list-posts.md)
- [List Space Members](actions/list-space-members.md)
- [List Spaces](actions/list-spaces.md)
