# Front Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Front expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-assigned-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0&teammateId=tea_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Front actions that support pagination

- [List Assigned Conversations](actions/list-assigned-conversations.md)
- [List Contact Conversations](actions/list-contact-conversations.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversation Drafts](actions/list-conversation-drafts.md)
- [List Conversation Messages](actions/list-conversation-messages.md)
- [List Conversations](actions/list-conversations.md)
- [List Tags](actions/list-tags.md)
- [List Views](actions/list-views.md)
- [Search Conversations](actions/search-conversations.md)
