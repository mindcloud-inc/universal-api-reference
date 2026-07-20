# Conexteo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Conexteo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contacts-in-contact-list?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Conexteo actions that support pagination

- [List Contacts In Contact List](actions/list-contacts-in-contact-list.md)
- [List Message History](actions/list-message-history.md)
- [List Message Replies](actions/list-message-replies.md)
- [List Stops](actions/list-stops.md)
