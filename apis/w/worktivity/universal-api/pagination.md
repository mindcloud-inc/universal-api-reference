# Worktivity Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Worktivity expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/get-application-usage-summary?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Worktivity actions that support pagination

- [Get Application Usage Summary](actions/get-application-usage-summary.md)
- [List Customers](actions/list-customers.md)
- [List Employees](actions/list-employees.md)
- [List Manual Time Entries](actions/list-manual-time-entries.md)
- [List Project Task Comments](actions/list-project-task-comments.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Screenshots](actions/list-screenshots.md)
- [List Teams](actions/list-teams.md)
