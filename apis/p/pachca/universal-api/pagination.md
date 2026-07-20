# Pachca Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pachca expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/list-chat-members?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pachca actions that support pagination

- [List chat members](actions/list-chat-members.md)
- [List chats](actions/list-chats.md)
- [List custom properties](actions/list-custom-properties.md)
- [List group tag users](actions/list-group-tag-users.md)
- [List group tags](actions/list-group-tags.md)
- [List messages](actions/list-messages.md)
- [List tasks](actions/list-tasks.md)
- [List users](actions/list-users.md)
- [Search chats](actions/search-chats.md)
- [Search messages](actions/search-messages.md)
- [Search users](actions/search-users.md)
