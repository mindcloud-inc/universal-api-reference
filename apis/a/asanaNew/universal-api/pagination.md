# Asana Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Asana expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-projects-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0&projectGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Asana actions that support pagination

- [Get a project's custom fields](actions/get-a-projects-custom-fields.md)
- [Get a task's tags](actions/get-a-tasks-tags.md)
- [Get a team's projects](actions/get-a-teams-projects.md)
- [Get a user's favorites](actions/get-a-users-favorites.md)
- [Get all projects in a workspace](actions/get-all-projects-in-a-workspace.md)
- [Get attachments from an object](actions/get-attachments-from-an-object.md)
- [Get dependencies from a task](actions/get-dependencies-from-a-task.md)
- [Get dependents from a task](actions/get-dependents-from-a-task.md)
- [Get goal relationships](actions/get-goal-relationships.md)
- [Get memberships from a portfolio](actions/get-memberships-from-a-portfolio.md)
- [Get memberships from a project](actions/get-memberships-from-a-project.md)
- [Get memberships from a team](actions/get-memberships-from-a-team.md)
- [Get memberships from a user](actions/get-memberships-from-a-user.md)
- [Get multiple portfolios](actions/get-multiple-portfolios.md)
- [Get multiple project templates](actions/get-multiple-project-templates.md)
- [Get multiple projects](actions/get-multiple-projects.md)
- [Get multiple tags](actions/get-multiple-tags.md)
- [Get multiple tasks](actions/get-multiple-tasks.md)
- [Get multiple webhooks](actions/get-multiple-webhooks.md)
- [Get multiple workspaces](actions/get-multiple-workspaces.md)
- [Get portfolio items](actions/get-portfolio-items.md)
- [Get sections in a project](actions/get-sections-in-a-project.md)
- [Get status updates from an object](actions/get-status-updates-from-an-object.md)
- [Get stories from a task](actions/get-stories-from-a-task.md)
- [Get subtasks from a task](actions/get-subtasks-from-a-task.md)
- [Get tags in a workspace](actions/get-tags-in-a-workspace.md)
- [Get tasks from a section](actions/get-tasks-from-a-section.md)
- [Get tasks from a user task list](actions/get-tasks-from-a-user-task-list.md)
- [Get workspace memberships for a user](actions/get-workspace-memberships-for-a-user.md)
