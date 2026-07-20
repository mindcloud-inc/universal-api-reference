# <img src="https://images.mindcloud.co/apps/icons/taskade_1774023920715.png" alt="Taskade logo" width="28" height="28"> Taskade: Universal API

Manage Taskade workspaces, projects, tasks, and AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/taskade/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.taskade.com
- **Vendor API docs:** https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent in Folder](actions/create-agent-in-folder.md) | POST | Creates a new Taskade agent in a folder. |
| [Generate Agent in Folder](actions/generate-agent-in-folder.md) | POST | Generates a Taskade agent from text in a folder. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves a single agent from Taskade. |
| [List Folder Agents](actions/list-folder-agents.md) | GET | Retrieves agents from a Taskade folder. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Taskade. |

### Agent Knowledge Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project To Agent Knowledge](actions/add-project-to-agent-knowledge.md) | POST | Adds a project to a Taskade agent knowledge base. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Folders](actions/list-workspace-folders.md) | GET | Retrieves folders from a Taskade workspace. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Media Files](actions/list-folder-media-files.md) | GET | Retrieves media files from a Taskade folder. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Copy Project](actions/copy-project.md) | POST | Copies a Taskade project into a folder. |
| [Create Project](actions/create-project.md) | POST | Creates a new Taskade project in a folder. |
| [Create Project in Workspace](actions/create-project-in-workspace.md) | POST | Creates a new Taskade project in a workspace. |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project from Taskade. |
| [List Folder Projects](actions/list-folder-projects.md) | GET | Retrieves projects from a Taskade folder. |
| [List My Projects](actions/list-my-projects.md) | GET | Retrieves your personal projects from Taskade. |

### Project Field

| Action | Method | Description |
| --- | --- | --- |
| [List Project Fields](actions/list-project-fields.md) | GET | Retrieves fields from a Taskade project. |

### Project Member

| Action | Method | Description |
| --- | --- | --- |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves members from a Taskade project. |

### Project Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Share Link](actions/get-project-share-link.md) | GET | Retrieves a share link for a Taskade project. |

### Project Template

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Project Templates](actions/list-folder-project-templates.md) | GET | Retrieves project templates from a Taskade folder. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in a Taskade project. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from a Taskade project. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves tasks from a Taskade project. |
| [Move Task](actions/move-task.md) | PUT | Moves a task within a Taskade project. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in a Taskade project. |

### Task Assignee

| Action | Method | Description |
| --- | --- | --- |
| [List Task Assignees](actions/list-task-assignees.md) | GET | Retrieves assignees for a Taskade task. |
| [Update Task Assignees](actions/update-task-assignees.md) | PUT | Updates assignees for a Taskade task. |

### Task Date

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Date](actions/get-task-date.md) | GET | Retrieves date details for a Taskade task. |
| [Update Task Date](actions/update-task-date.md) | PUT | Updates date details for a Taskade task. |

### Task Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Note](actions/get-task-note.md) | GET | Retrieves the note for a Taskade task. |
| [Update Task Note](actions/update-task-note.md) | PUT | Updates the note for a Taskade task. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from your Taskade account. |

