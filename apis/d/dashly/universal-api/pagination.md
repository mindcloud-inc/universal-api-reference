# Dashly Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Dashly expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/get-conversation-parts?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Dashly actions that support pagination

- [Get Conversation Parts](actions/get-conversation-parts.md)
- [List Active Users](actions/list-active-users.md)
- [List App Conversations](actions/list-app-conversations.md)
- [List User Conversations](actions/list-user-conversations.md)
- [List User Events](actions/list-user-events.md)
