# HelpCrunch Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model HelpCrunch expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## HelpCrunch actions that support pagination

- [List Chat Messages](actions/list-chat-messages.md)
- [List Chats](actions/list-chats.md)
- [List Customers](actions/list-customers.md)
- [Search Chats](actions/search-chats.md)
- [Search Customers](actions/search-customers.md)
