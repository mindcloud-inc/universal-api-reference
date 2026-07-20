# <img src="https://images.mindcloud.co/apps/icons/pm_1775059465002.png" alt="5pm logo" width="28" height="28"> 5pm: Universal API

5pm is a project management platform for projects, tasks, users, groups, activities, and file attachments through the 5pm API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pm/latest
- **Category:** Productivity / Project Management
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.5pmweb.com
- **Vendor API docs:** https://www.5pmweb.com/help/api_docs.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Statuses](actions/list-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in 5pm. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from 5pm. |
| [Remove Activity](actions/remove-activity.md) | DELETE | Deletes an existing activity from 5pm. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in 5pm. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Attach Files](actions/attach-files.md) | POST | Uploads files to an activity in 5pm. |
| [Download File](actions/download-file.md) | GET | Downloads an activity file from 5pm. |
| [List Files](actions/list-files.md) | GET | Retrieves activity files from 5pm. |
| [Remove File](actions/remove-file.md) | DELETE | Deletes an activity file from 5pm. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new project group in 5pm. |
| [List All Groups](actions/list-all-groups.md) | GET | Retrieves all project groups from 5pm. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing project group in 5pm. |

### Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves task priorities from 5pm. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in 5pm. |
| [Get Project By Id](actions/get-project-by-id.md) | GET | Retrieves a project from 5pm by ID. |
| [List All Projects](actions/list-all-projects.md) | GET | Retrieves all projects from 5pm. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from 5pm. |
| [Remove Project](actions/remove-project.md) | DELETE | Deletes an existing project from 5pm. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in 5pm. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Sign In](actions/sign-in.md) | GET | Signs in to 5pm and returns a session ID. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves project statuses from 5pm. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in 5pm. |
| [Get Task By Id](actions/get-task-by-id.md) | GET | Retrieves a task from 5pm by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from 5pm. |
| [Remove Task](actions/remove-task.md) | DELETE | Deletes an existing task from 5pm. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in 5pm. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in 5pm. |
| [Get User By Email](actions/get-user-by-email.md) | GET | Retrieves a user from 5pm by email address. |
| [Get User By Id](actions/get-user-by-id.md) | GET | Retrieves a user from 5pm by ID. |
| [List All Users](actions/list-all-users.md) | GET | Retrieves all users from 5pm. |
| [Remove User](actions/remove-user.md) | DELETE | Deletes an existing user from 5pm. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in 5pm. |

