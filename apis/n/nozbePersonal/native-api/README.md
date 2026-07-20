# Nozbe Personal: Native API Reference

A consolidated summary of Nozbe Personal's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://api4.nozbe.com/v1/api
- **OpenAPI specification:** https://api4.nozbe.com/v1/api/openapi.yaml
- **API base URL:** `https://api4.nozbe.com/v1/api`

## Authentication

### API Token

Connect with a Nozbe API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://nozbe.help/advancedfeatures/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `min`, `ne`.

## Sorting

Set the sort field with `sortBy` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://api4.nozbe.com/v1/api#/comments/postComment) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api4.nozbe.com/v1/api#/projects/postProject) |
| [Create Project From Template](actions/create-project-from-template.md) | `POST /projects/from_template/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/postProjectFromTemplate) |
| [Create Project Section](actions/create-project-section.md) | `POST /project_sections` | [docs](https://api4.nozbe.com/v1/api#/project_sections/postProjectSection) |
| [Create Reminder](actions/create-reminder.md) | `POST /reminders` | [docs](https://api4.nozbe.com/v1/api#/reminders/postReminder) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://api4.nozbe.com/v1/api#/tags/postTag) |
| [Create Tag Assignment](actions/create-tag-assignment.md) | `POST /tag_assignments` | [docs](https://api4.nozbe.com/v1/api#/tag_assignments/postTagAssignment) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://api4.nozbe.com/v1/api#/tasks/postTask) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/deleteCommentById) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/deleteProjectById) |
| [Delete Project Section](actions/delete-project-section.md) | `DELETE /project_sections/:id` | [docs](https://api4.nozbe.com/v1/api#/project_sections/deleteProjectSectionById) |
| [Delete Reminder](actions/delete-reminder.md) | `DELETE /reminders/:id` | [docs](https://api4.nozbe.com/v1/api#/reminders/deleteReminderById) |
| [Delete Tag Assignment](actions/delete-tag-assignment.md) | `DELETE /tag_assignments/:id` | [docs](https://api4.nozbe.com/v1/api#/tag_assignments/deleteTagAssignmentById) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/deleteTaskById) |
| [Download Attachment Content](actions/download-attachment-content.md) | `GET /comments/:comment_id/attachments/:file_id/content` | [docs](https://api4.nozbe.com/v1/api#/attachments/getattachmentByIdContent) |
| [Get Comment](actions/get-comment.md) | `GET /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/getCommentById) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/getProjectById) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/getTaskById) |
| [Get Team](actions/get-team.md) | `GET /teams/:id` | [docs](https://api4.nozbe.com/v1/api#/teams/getTeamById) |
| [List Comment Attachments](actions/list-comment-attachments.md) | `GET /comments/:comment_id/attachments` | [docs](https://api4.nozbe.com/v1/api#/attachments/getattachments) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://api4.nozbe.com/v1/api#/comments/getComments) |
| [List Project Sections](actions/list-project-sections.md) | `GET /project_sections` | [docs](https://api4.nozbe.com/v1/api#/project_sections/getProjectSections) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api4.nozbe.com/v1/api#/projects/getProjects) |
| [List Reminders](actions/list-reminders.md) | `GET /reminders` | [docs](https://api4.nozbe.com/v1/api#/reminders/getReminders) |
| [List Tag Assignments](actions/list-tag-assignments.md) | `GET /tag_assignments` | [docs](https://api4.nozbe.com/v1/api#/tag_assignments/getTagAssignments) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api4.nozbe.com/v1/api#/tags/getTags) |
| [List Task Recurrences](actions/list-task-recurrences.md) | `GET /task_recurrences` | [docs](https://api4.nozbe.com/v1/api#/task_recurrences/getTaskRecurrences) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://api4.nozbe.com/v1/api#/tasks/getTasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://api4.nozbe.com/v1/api#/teams/getTeams) |
| [Update Comment](actions/update-comment.md) | `PUT /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/putCommentById) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/putProjectById) |
| [Update Project Section](actions/update-project-section.md) | `PUT /project_sections/:id` | [docs](https://api4.nozbe.com/v1/api#/project_sections/putProjectSectionById) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:id` | [docs](https://api4.nozbe.com/v1/api#/tags/putTagById) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/putTaskById) |
| [Upload Attachment With Content](actions/upload-attachment-with-content.md) | `POST /comments/:comment_id/attachment_with_content` | [docs](https://api4.nozbe.com/v1/api#/attachments/postattachmentByIdContent2) |
