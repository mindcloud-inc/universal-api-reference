# SurveySparrow Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SurveySparrow expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-audit-log-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SurveySparrow actions that support pagination

- [List Audit Log Events](actions/list-audit-log-events.md)
- [List Audit Logs](actions/list-audit-logs.md)
- [List Channels](actions/list-channels.md)
- [List Contacts](actions/list-contacts.md)
- [List Expressions](actions/list-expressions.md)
- [List Questions](actions/list-questions.md)
- [List Responses](actions/list-responses.md)
- [List Roles](actions/list-roles.md)
- [List Survey Folders](actions/list-survey-folders.md)
- [List Surveys](actions/list-surveys.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)
- [List Variables](actions/list-variables.md)
- [List Webhooks](actions/list-webhooks.md)
