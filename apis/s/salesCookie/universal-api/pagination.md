# Sales Cookie Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Sales Cookie expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Sales Cookie actions that support pagination

- [List Alerts](actions/list-alerts.md)
- [List Announcements](actions/list-announcements.md)
- [List Calculation Commissions](actions/list-calculation-commissions.md)
- [List Calculation Credits](actions/list-calculation-credits.md)
- [List Calculation Results](actions/list-calculation-results.md)
- [List Catalog Entries](actions/list-catalog-entries.md)
- [List Custom Variables](actions/list-custom-variables.md)
- [List Event Logs](actions/list-event-logs.md)
- [List Plan Enrollments](actions/list-plan-enrollments.md)
- [List Plan Roles](actions/list-plan-roles.md)
- [List Plans](actions/list-plans.md)
- [List Reports](actions/list-reports.md)
- [List Survey Results](actions/list-survey-results.md)
- [List Surveys](actions/list-surveys.md)
- [List Team Aliases](actions/list-team-aliases.md)
- [List Team Members](actions/list-team-members.md)
- [List Teams](actions/list-teams.md)
- [List Transactions](actions/list-transactions.md)
- [List User Aliases](actions/list-user-aliases.md)
- [List Users](actions/list-users.md)
- [List Workspace Roles](actions/list-workspace-roles.md)
- [List Workspace Settings](actions/list-workspace-settings.md)
