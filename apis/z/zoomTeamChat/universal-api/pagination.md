# Zoom Team Chat Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoom Team Chat expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-accounts-public-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoom Team Chat actions that support pagination

- [List Account's Public Channels](actions/list-accounts-public-channels.md)
- [List Channel Activity Logs](actions/list-channel-activity-logs.md)
- [List Channel Administrators](actions/list-channel-administrators.md)
- [List Channel Members](actions/list-channel-members.md)
- [List Members Of A Mention Group](actions/list-members-of-a-mention-group.md)
- [List Reminders](actions/list-reminders.md)
- [List Shared Space Channels](actions/list-shared-space-channels.md)
- [List Shared Spaces](actions/list-shared-spaces.md)
- [List User's Channels](actions/list-user-channels.md)
- [List User's Chat Messages](actions/list-users-chat-messages.md)
- [List User's Chat Sessions](actions/list-users-chat-sessions.md)
- [List User's Contacts](actions/list-users-contacts.md)
- [Search Company Contacts](actions/search-company-contacts.md)
