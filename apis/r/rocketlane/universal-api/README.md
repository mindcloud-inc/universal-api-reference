# <img src="https://images.mindcloud.co/apps/icons/3052908458180-f318530a91fe13584e70-512_1773776870938.png" alt="Rocketlane logo" width="28" height="28"> Rocketlane: Universal API

Manage Rocketlane projects, tasks, conversations, and time entries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rocketlane/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rocketlane.com
- **Vendor API docs:** https://developer.rocketlane.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment in Rocketlane. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a comment from Rocketlane. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Rocketlane. |
| [List Comments](actions/list-comments.md) | GET | Lists comments in Rocketlane. |
| [Update Comment](actions/update-comment.md) | PUT | Updates a comment in Rocketlane. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Members](actions/add-conversation-members.md) | PUT | Adds members to a conversation in Rocketlane. |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a conversation in Rocketlane. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Rocketlane. |
| [List Conversations](actions/list-conversations.md) | GET | Lists conversations in Rocketlane. |
| [Remove Conversation Members](actions/remove-conversation-members.md) | PUT | Removes members from a conversation in Rocketlane. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates a conversation in Rocketlane. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Lists invoices in Rocketlane. |

### Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Phase](actions/create-phase.md) | POST | Creates a phase in Rocketlane. |
| [Delete Phase](actions/delete-phase.md) | DELETE | Deletes a phase from Rocketlane. |
| [Get Phase](actions/get-phase.md) | GET | Retrieves a phase from Rocketlane. |
| [List Phases](actions/list-phases.md) | GET | Lists phases in Rocketlane. |
| [Update Phase](actions/update-phase.md) | PUT | Updates a phase in Rocketlane. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Members](actions/add-project-members.md) | PUT | Adds members to a project in Rocketlane. |
| [Archive Project](actions/archive-project.md) | PUT | Archives a project in Rocketlane. |
| [Create Project](actions/create-project.md) | POST | Creates a project in Rocketlane. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Rocketlane. |
| [Import Project Template](actions/import-project-template.md) | PUT | Imports a project template into Rocketlane. |
| [List Projects](actions/list-projects.md) | GET | Lists projects in Rocketlane. |
| [Remove Project Members](actions/remove-project-members.md) | PUT | Removes members from a project in Rocketlane. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Rocketlane. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Assignees](actions/add-task-assignees.md) | PUT | Adds assignees to a task in Rocketlane. |
| [Add Task Dependencies](actions/add-task-dependencies.md) | PUT | Adds dependencies to a task in Rocketlane. |
| [Create Task](actions/create-task.md) | POST | Creates a task in Rocketlane. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from Rocketlane. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Rocketlane. |
| [List Tasks](actions/list-tasks.md) | GET | Lists tasks in Rocketlane. |
| [Move Task To Phase](actions/move-task-to-phase.md) | PUT | Moves a task to a phase in Rocketlane. |
| [Remove Task Assignees](actions/remove-task-assignees.md) | PUT | Removes assignees from a task in Rocketlane. |
| [Remove Task Dependencies](actions/remove-task-dependencies.md) | PUT | Removes dependencies from a task in Rocketlane. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Rocketlane. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Rocketlane. |
| [List Time Entries](actions/list-time-entries.md) | GET | Lists time entries in Rocketlane. |
| [Search Time Entries](actions/search-time-entries.md) | GET | Searches time entries in Rocketlane. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Rocketlane. |
| [List Users](actions/list-users.md) | GET | Lists users in Rocketlane. |

