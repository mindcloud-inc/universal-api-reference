# Automate Team - Task Management Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Automate Team - Task Management expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceFilter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Automate Team - Task Management actions that support pagination

- [List Categories](actions/list-categories.md)
- [List Task Users](actions/list-task-users.md)
- [List Tasks](actions/list-tasks.md)
