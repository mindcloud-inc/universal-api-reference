# WebWork Time Tracker Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WebWork Time Tracker expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WebWork Time Tracker actions that support pagination

- [List Contracts](actions/list-contracts.md)
- [List Expenses](actions/list-expenses.md)
- [List Leaves](actions/list-leaves.md)
- [List Members](actions/list-members.md)
- [List Projects](actions/list-projects.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Time Requests](actions/list-time-requests.md)
- [List Timesheets](actions/list-timesheets.md)
- [List Workspaces](actions/list-workspaces.md)
