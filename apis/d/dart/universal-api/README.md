# <img src="https://images.mindcloud.co/apps/icons/dart-management_1774624573966.png" alt="Dart logo" width="28" height="28"> Dart: Universal API

AI-native project management platform for tasks, docs, comments, views, folders, and dartboards via the Dart Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dart/latest
- **Category:** Productivity / Project Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dartai.com
- **Vendor API docs:** https://app.dartai.com/api/v0/public/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Space Configuration](actions/get-user-space-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Attachment From Url](actions/add-task-attachment-from-url.md) | POST | Adds a URL attachment to a Dart task. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Get Dartboard](actions/get-dartboard.md) | GET | Retrieves a dartboard record from Dart. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST | Creates a task comment in Dart. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves task comments from Dart with pagination. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Doc](actions/create-doc.md) | POST | Creates a new doc in Dart. |
| [Delete Doc](actions/delete-doc.md) | DELETE | Deletes an existing doc from Dart. |
| [Get Doc](actions/get-doc.md) | GET | Retrieves a doc record from Dart. |
| [List Docs](actions/list-docs.md) | GET | Retrieves docs from Dart with optional title filtering. |
| [Update Doc](actions/update-doc.md) | PUT | Updates an existing doc in Dart. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder record from Dart. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [List Help Center Articles](actions/list-help-center-articles.md) | GET | Retrieves help center articles from Dart. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Dart. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Dart. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task record from Dart. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Dart with optional filters. |
| [Move Task](actions/move-task.md) | PUT | Moves a task within a Dart dartboard. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Dart. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Skill by Title](actions/retrieve-skill-by-title.md) | GET | Retrieves a skill from Dart by title. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Time Tracking Entry](actions/add-task-time-tracking-entry.md) | POST | Adds a time tracking entry to a Dart task. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get View](actions/get-view.md) | GET | Retrieves a view record from Dart. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get User Space Configuration](actions/get-user-space-configuration.md) | GET | Retrieves user space configuration details from Dart. |

