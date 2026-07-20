# SuperSend Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SuperSend expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SuperSend actions that support pagination

- [Get Conversation Messages](actions/get-conversation-messages.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Contact Profile Labels](actions/list-contact-profile-labels.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversations](actions/list-conversations.md)
- [List Events](actions/list-events.md)
- [List Placement Tests](actions/list-placement-tests.md)
- [List Senders](actions/list-senders.md)
- [List Teams](actions/list-teams.md)
