# Smart Sender Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Smart Sender expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-contact-gates?connectionId=$CONNECTION_ID&limit=25&offset=0&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Smart Sender actions that support pagination

- [Get Contact Gates](actions/get-contact-gates.md)
- [List Channels](actions/list-channels.md)
- [List Chat Messages](actions/list-chat-messages.md)
- [List Chats](actions/list-chats.md)
- [List Contact Funnels](actions/list-contact-funnels.md)
- [List Contact Messages](actions/list-contact-messages.md)
- [List Contact Tags](actions/list-contact-tags.md)
- [List Contacts](actions/list-contacts.md)
- [List Products](actions/list-products.md)
- [List Variables](actions/list-variables.md)
- [Search Contacts](actions/search-contacts.md)
