# Microsoft Teams Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Microsoft Teams expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&teamId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Microsoft Teams actions that support pagination

- [List Channel Messages](actions/list-channel-messages.md)
- [List Chat Messages](actions/list-chat-messages.md)
- [List Chats](actions/list-chats.md)
