# YouGile Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model YouGile expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## YouGile actions that support pagination

- [List boards](actions/list-boards.md)
- [List chat messages](actions/list-chat-messages.md)
- [List columns](actions/list-columns.md)
- [List group chats](actions/list-group-chats.md)
- [List projects](actions/list-projects.md)
- [List recent tasks](actions/list-recent-tasks.md)
- [List tasks](actions/list-tasks.md)
- [List users](actions/list-users.md)
