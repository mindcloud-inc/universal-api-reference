# Umbler Talk Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Umbler Talk expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-chats?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Umbler Talk actions that support pagination

- [List Chats](actions/list-chats.md)
- [List Contact Chats](actions/list-contact-chats.md)
- [List Contacts](actions/list-contacts.md)
- [List Quick Answers](actions/list-quick-answers.md)
- [List Tags](actions/list-tags.md)
