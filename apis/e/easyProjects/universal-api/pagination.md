# Easy Projects Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Easy Projects expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Easy Projects actions that support pagination

- [Get All Projects](actions/get-all-projects.md)
- [Get All Tasks](actions/get-all-tasks.md)
- [Get All Teams](actions/get-all-teams.md)
- [Get All Users](actions/get-all-users.md)
- [Get Customers](actions/get-customers.md)
- [Get My Active Tasks](actions/get-my-active-tasks.md)
- [Get My In Progress Tasks](actions/get-my-in-progress-tasks.md)
- [Get My Tasks](actions/get-my-tasks.md)
- [Get Priorities](actions/get-priorities.md)
- [Get Project Attachments](actions/get-project-attachments.md)
- [Get Project Kanban](actions/get-project-kanban.md)
- [Get Project Members](actions/get-project-members.md)
- [Get Project Messages](actions/get-project-messages.md)
- [Get Project Statuses](actions/get-project-statuses.md)
- [Get Project Tasks](actions/get-project-tasks.md)
- [Get Task Attachments](actions/get-task-attachments.md)
- [Get Task Messages](actions/get-task-messages.md)
- [Get Task Statuses](actions/get-task-statuses.md)
- [Get Task Types](actions/get-task-types.md)
- [Get Tasks By Projects](actions/get-tasks-by-projects.md)
