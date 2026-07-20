# Clockify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Clockify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-in-progress-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Clockify actions that support pagination

- [List In-Progress Time Entries](actions/list-in-progress-time-entries.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List User Time Entries](actions/list-user-time-entries.md)
- [List Workspace Clients](actions/list-workspace-clients.md)
- [List Workspace Projects](actions/list-workspace-projects.md)
- [List Workspace Tags](actions/list-workspace-tags.md)
- [List Workspace Users](actions/list-workspace-users.md)
