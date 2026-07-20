# <img src="https://images.mindcloud.co/apps/icons/pm-logo-email_1775827098429.png" alt="ProjectManager logo" width="28" height="28"> ProjectManager: Universal API

Production-ready ProjectManager wrapper built from official REST API documentation with API key authentication and a curated 40-action catalog for projects, tasks, tags, resources, meetings, notifications, and risks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/projectManager/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.projectmanager.com
- **Vendor API docs:** https://developer.projectmanager.com/getting-started/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Me](actions/retrieve-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Me](actions/retrieve-me.md) | GET | Retrieves current user details from ProjectManager. |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST | Creates a new meeting in ProjectManager. |
| [Get Meeting](actions/get-meeting.md) | GET | Retrieves a meeting from ProjectManager. |
| [Update Meeting](actions/update-meeting.md) | PUT | Updates an existing meeting in ProjectManager. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Mark Notification Read](actions/mark-notification-read.md) | POST | Marks a notification as read in ProjectManager. |
| [Retrieve Notifications](actions/retrieve-notifications.md) | GET | Retrieves notifications from ProjectManager. |
| [Unread Notification Count](actions/unread-notification-count.md) | GET | Retrieves unread notification count from ProjectManager. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in ProjectManager. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from ProjectManager. |
| [Query Projects](actions/query-projects.md) | GET | Finds projects in ProjectManager. |
| [Restore Project](actions/restore-project.md) | PUT | Restores a deleted project in ProjectManager. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from ProjectManager. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in ProjectManager. |

### Project Priority

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Project Priorities](actions/retrieve-project-priorities.md) | GET | Retrieves project priorities from ProjectManager. |

### Project Template

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Project Templates](actions/retrieve-project-templates.md) | GET | Retrieves project templates from ProjectManager. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in ProjectManager. |
| [Query Resources](actions/query-resources.md) | GET | Finds resources in ProjectManager. |
| [Retrieve Resource](actions/retrieve-resource.md) | GET | Retrieves a resource from ProjectManager. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in ProjectManager. |

### Risk

| Action | Method | Description |
| --- | --- | --- |
| [Get Risk](actions/get-risk.md) | GET | Retrieves a risk from ProjectManager. |
| [Query Risks](actions/query-risks.md) | GET | Finds risks in ProjectManager. |
| [Update Risk](actions/update-risk.md) | PUT | Updates an existing risk in ProjectManager. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in ProjectManager. |
| [Query Tags](actions/query-tags.md) | GET | Finds tags in ProjectManager. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in ProjectManager. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in ProjectManager. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from ProjectManager. |
| [Fetch the first level child tasks from the task](actions/fetch-the-first-level-child-tasks-from-the-task.md) | GET | Retrieves first-level subtasks from a task in ProjectManager. |
| [Query Tasks](actions/query-tasks.md) | GET | Finds tasks in ProjectManager. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from ProjectManager. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in ProjectManager. |

### Task Assignee

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update TaskAssignee](actions/create-or-update-task-assignee.md) | PUT | Creates or updates task assignees in ProjectManager. |
| [Returns task assignees](actions/returns-task-assignees.md) | GET | Retrieves task assignees from ProjectManager. |

### Task Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST | Creates a new task comment in ProjectManager. |
| [Retrieve Task Comments](actions/retrieve-task-comments.md) | GET | Retrieves task comments from ProjectManager. |

### Task Priority

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Task Priorities](actions/retrieve-task-priorities.md) | GET | Retrieves task priorities from ProjectManager. |

### Task Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add TaskTag to Task](actions/add-task-tag-to-task.md) | PUT | Adds a task tag to a task in ProjectManager. |
| [Remove TaskTag from Task](actions/remove-task-tag-from-task.md) | DELETE | Removes a task tag from a task in ProjectManager. |
| [Retrieve TaskTags](actions/retrieve-task-tags.md) | GET | Retrieves task tags from ProjectManager. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Workspaces](actions/retrieve-workspaces.md) | GET | Retrieves workspaces from ProjectManager. |

