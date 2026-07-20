# Are.na Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Are.na expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/list-block-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Are.na actions that support pagination

- [List Block Comments](actions/list-block-comments.md)
- [List Block Connections](actions/list-block-connections.md)
- [List Channel Connections](actions/list-channel-connections.md)
- [List Channel Contents](actions/list-channel-contents.md)
- [List Channel Followers](actions/list-channel-followers.md)
- [List Group Contents](actions/list-group-contents.md)
- [List Group Followers](actions/list-group-followers.md)
- [List User Contents](actions/list-user-contents.md)
- [List User Followers](actions/list-user-followers.md)
- [List User Following](actions/list-user-following.md)
- [List User Groups](actions/list-user-groups.md)
- [Search Are.na](actions/search-arena.md)
