# <img src="https://images.mindcloud.co/apps/icons/bug-herd_1782741403862.png" alt="BugHerd logo" width="28" height="28"> BugHerd: Universal API

Website feedback and bug tracking for development teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bugHerd/latest
- **Category:** Support / Ticketing
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bugherd.com
- **Vendor API docs:** https://docs.bugherd.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Show Organization](actions/show-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/show-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment From URL](actions/create-attachment-from-url.md) | POST | Creates a task attachment from a URL in BugHerd. |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from a BugHerd task. |
| [Show Attachment](actions/show-attachment.md) | GET | Retrieves an attachment from a BugHerd task. |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to a BugHerd task. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | POST | Creates a new column in a BugHerd project. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment on a BugHerd task. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from a BugHerd task. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Show Organization](actions/show-organization.md) | GET | Retrieves organization details from BugHerd. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an attachment from a BugHerd task. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from BugHerd. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from BugHerd. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from BugHerd. |
| [List Columns](actions/list-columns.md) | GET | Retrieves columns from a BugHerd project. |
| [List Members](actions/list-members.md) | GET | Retrieves members from BugHerd. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves projects for a BugHerd user. |
| [List User Tasks](actions/list-user-tasks.md) | GET | Retrieves tasks for a BugHerd user. |
| [List Users](actions/list-users.md) | GET | Retrieves users from BugHerd. |
| [Show Column](actions/show-column.md) | GET | Retrieves a column from a BugHerd project. |
| [Update Column](actions/update-column.md) | PUT | Updates an existing column in a BugHerd project. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in BugHerd. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in BugHerd. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in BugHerd. |
| [List Active Projects](actions/list-active-projects.md) | GET | Retrieves active projects from BugHerd. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from BugHerd. |
| [Show Project](actions/show-project.md) | GET | Retrieves a project from BugHerd. |

### Project Client

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Client](actions/add-project-client.md) | POST | Adds a client to a BugHerd project. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | POST | Adds a member to a BugHerd project. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in BugHerd. |
| [List Archived Tasks](actions/list-archived-tasks.md) | GET | Retrieves archived tasks from a BugHerd project. |
| [List Feedback Tasks](actions/list-feedback-tasks.md) | GET | Retrieves feedback tasks from a BugHerd project. |
| [List Taskboard Tasks](actions/list-taskboard-tasks.md) | GET | Retrieves taskboard tasks from a BugHerd project. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from a BugHerd project. |
| [Show Task By Global ID](actions/show-task-by-global-id.md) | GET | Retrieves a BugHerd task by global ID. |
| [Show Task By Local Task ID](actions/show-task-by-local-task-id.md) | GET | Retrieves a BugHerd task by local task ID. |
| [Show Task By Project ID](actions/show-task-by-project-id.md) | GET | Retrieves a task from a BugHerd project. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in BugHerd. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from BugHerd. |

