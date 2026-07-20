# <img src="https://images.mindcloud.co/apps/icons/redbooth_1773950729478.png" alt="Redbooth logo" width="28" height="28"> Redbooth: Universal API

Redbooth project management API integration for organizations, projects, task lists, tasks, comments, conversations, time entries, search, and web hooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/redbooth/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://redbooth.com/
- **Vendor API docs:** https://redbooth.com/api/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Information](actions/get-user-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Redbooth. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Redbooth. |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes an existing conversation from Redbooth. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Redbooth. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Redbooth. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Redbooth. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Redbooth. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Redbooth. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Redbooth. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Redbooth. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Redbooth. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Redbooth. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds matching records in your Redbooth account. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Redbooth. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Redbooth. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Redbooth. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Redbooth. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Redbooth. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [Create Task List](actions/create-task-list.md) | POST | Creates a new task list in Redbooth. |
| [Delete Task List](actions/delete-task-list.md) | DELETE | Deletes an existing task list from Redbooth. |
| [Get Task List](actions/get-task-list.md) | GET | Retrieves a task list from Redbooth. |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from Redbooth. |
| [Update Task List](actions/update-task-list.md) | PUT | Updates an existing task list in Redbooth. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves the current user's information from Redbooth. |

