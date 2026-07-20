# Timetoreply Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Timetoreply expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/get-comparative-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Timetoreply actions that support pagination

- [Get Comparative Report](actions/get-comparative-report.md)
- [Get Group Mailboxes Report](actions/get-group-mailboxes-report.md)
- [Get Interactions Report](actions/get-interactions-report.md)
- [Get Productivity Report](actions/get-productivity-report.md)
- [Get Teams Report](actions/get-teams-report.md)
- [List Agent Alerts](actions/list-agent-alerts.md)
- [List Contact Groups](actions/list-contact-groups.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversation Logs](actions/list-conversation-logs.md)
- [List Group Mailboxes](actions/list-group-mailboxes.md)
- [List Mailboxes](actions/list-mailboxes.md)
- [List Message Logs](actions/list-message-logs.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)
