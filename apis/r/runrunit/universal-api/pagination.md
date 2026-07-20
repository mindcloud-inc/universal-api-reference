# Runrun.it Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Runrun.it expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Runrun.it actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Clients](actions/list-clients.md)
- [List Project Groups](actions/list-project-groups.md)
- [List Project Sub Groups](actions/list-project-sub-groups.md)
- [List Projects](actions/list-projects.md)
- [List Task Comments](actions/list-task-comments.md)
- [List Task Subtasks](actions/list-task-subtasks.md)
- [List Task Types](actions/list-task-types.md)
- [List Teams](actions/list-teams.md)
- [List Time Worked](actions/list-time-worked.md)
- [List Users](actions/list-users.md)
- [Search Tags](actions/search-tags.md)
- [Search Tasks](actions/search-tasks.md)
