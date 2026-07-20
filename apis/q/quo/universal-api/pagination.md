# Quo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Quo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0&participants%5B%5D=string&phoneNumberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Quo actions that support pagination

- [List Calls](actions/list-calls.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversations](actions/list-conversations.md)
- [List Messages](actions/list-messages.md)
- [List Users](actions/list-users.md)
