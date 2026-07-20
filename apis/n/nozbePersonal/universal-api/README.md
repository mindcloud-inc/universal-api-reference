# <img src="https://images.mindcloud.co/apps/icons/skdlfj_1774637741947.png" alt="Nozbe Personal logo" width="28" height="28"> Nozbe Personal: Universal API

Manage tasks, projects, comments, and team collaboration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nozbePersonal/latest
- **Category:** Productivity / Project Management
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nozbe.com
- **Vendor API docs:** https://api4.nozbe.com/v1/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment With Content](actions/upload-attachment-with-content.md) | POST | Uploads file content to create a Nozbe Personal attachment. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Download Attachment Content](actions/download-attachment-content.md) | GET | Retrieves attachment file content from Nozbe Personal. |
| [List Comment Attachments](actions/list-comment-attachments.md) | GET | Retrieves attachments for a Nozbe Personal comment. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Nozbe Personal. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Nozbe Personal. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Nozbe Personal by ID. |
| [List Comments](actions/list-comments.md) | GET | Retrieves accessible comments from Nozbe Personal. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Nozbe Personal. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Section](actions/delete-project-section.md) | DELETE | Deletes an existing project section from Nozbe Personal. |
| [Delete Reminder](actions/delete-reminder.md) | DELETE | Deletes an existing reminder from Nozbe Personal. |
| [Delete Tag Assignment](actions/delete-tag-assignment.md) | DELETE | Deletes an existing tag assignment from Nozbe Personal. |
| [List Project Sections](actions/list-project-sections.md) | GET | Retrieves accessible project sections from Nozbe Personal. |
| [List Tags](actions/list-tags.md) | GET | Retrieves accessible tags from Nozbe Personal. |
| [Update Project Section](actions/update-project-section.md) | PUT | Updates an existing project section in Nozbe Personal. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Nozbe Personal. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Nozbe Personal. |
| [Create Project From Template](actions/create-project-from-template.md) | POST | Creates a new project from a Nozbe Personal template. |
| [List Projects](actions/list-projects.md) | GET | Retrieves accessible projects from Nozbe Personal. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Nozbe Personal. |

### Project Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Section](actions/create-project-section.md) | POST | Creates a new project section in Nozbe Personal. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Nozbe Personal. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Nozbe Personal by ID. |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST | Creates a new reminder in Nozbe Personal. |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves accessible reminders from Nozbe Personal. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Nozbe Personal. |

### Tag Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag Assignment](actions/create-tag-assignment.md) | POST | Creates a new tag assignment in Nozbe Personal. |
| [List Tag Assignments](actions/list-tag-assignments.md) | GET | Retrieves accessible tag assignments from Nozbe Personal. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Nozbe Personal. |

### Task Recurrence

| Action | Method | Description |
| --- | --- | --- |
| [List Task Recurrences](actions/list-task-recurrences.md) | GET | Retrieves accessible task recurrences from Nozbe Personal. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Nozbe Personal. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Nozbe Personal by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves accessible tasks from Nozbe Personal. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Nozbe Personal. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Nozbe Personal by ID. |
| [List Teams](actions/list-teams.md) | GET | Retrieves accessible teams from Nozbe Personal. |

