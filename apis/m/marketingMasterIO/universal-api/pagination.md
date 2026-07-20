# Marketing Master IO Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Marketing Master IO expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chat-sequences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Marketing Master IO actions that support pagination

- [List Chat Sequences](actions/list-chat-sequences.md)
- [List Contact Books](actions/list-contact-books.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Variables](actions/list-custom-variables.md)
- [List Facebook Pages](actions/list-facebook-pages.md)
- [List Messenger Subscribers](actions/list-messenger-subscribers.md)
