# <img src="https://images.mindcloud.co/apps/icons/runrunit_1774361786013.png" alt="Runrun.it logo" width="28" height="28"> Runrun.it: Universal API

Manage Runrun.it tasks, projects, teams, and work tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/runrunit/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://runrun.it
- **Vendor API docs:** https://runrun.it/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Runrun.it. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Runrun.it. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Runrun.it. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Runrun.it. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Runrun.it. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Runrun.it. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a task in Runrun.it. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Change Project Board Stage](actions/change-project-board-stage.md) | PUT | Updates a project's board stage in Runrun.it. |
| [Clone Project](actions/clone-project.md) | POST | Creates a new project by cloning a Runrun.it project. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Runrun.it. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Runrun.it. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Runrun.it. |

### Project Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Group](actions/get-project-group.md) | GET | Retrieves a project group from Runrun.it. |
| [List Project Groups](actions/list-project-groups.md) | GET | Retrieves project groups from Runrun.it. |

### Project Subgroup

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Sub Group](actions/get-project-sub-group.md) | GET | Retrieves a project subgroup from Runrun.it. |
| [List Project Sub Groups](actions/list-project-sub-groups.md) | GET | Retrieves project subgroups from Runrun.it. |

### Project User

| Action | Method | Description |
| --- | --- | --- |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves users related to a project in Runrun.it. |

### Subtask

| Action | Method | Description |
| --- | --- | --- |
| [List Task Subtasks](actions/list-task-subtasks.md) | GET | Retrieves subtasks for a task in Runrun.it. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Search Tags](actions/search-tags.md) | GET | Finds tags in Runrun.it. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Runrun.it. |
| [Deliver Task](actions/deliver-task.md) | PUT | Delivers a task in Runrun.it. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Runrun.it. |
| [Move Task To Project](actions/move-task-to-project.md) | PUT | Updates a task's project in Runrun.it. |
| [Pause Task](actions/pause-task.md) | PUT | Pauses a task in Runrun.it. |
| [Reopen Task](actions/reopen-task.md) | PUT | Reopens a task in Runrun.it. |
| [Search Tasks](actions/search-tasks.md) | GET | Finds tasks in Runrun.it. |
| [Start Task](actions/start-task.md) | PUT | Starts a task in Runrun.it. |

### Task Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Type](actions/get-task-type.md) | GET | Retrieves a task type from Runrun.it. |
| [List Task Types](actions/list-task-types.md) | GET | Retrieves task types from Runrun.it. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Runrun.it. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Runrun.it. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Runrun.it. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in Runrun.it. |

### Team Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Team](actions/add-user-to-team.md) | PUT | Adds a user to a team in Runrun.it. |
| [Remove User From Team](actions/remove-user-from-team.md) | PUT | Removes a user from a team in Runrun.it. |

### Time Worked

| Action | Method | Description |
| --- | --- | --- |
| [List Time Worked](actions/list-time-worked.md) | GET | Retrieves time worked reports from Runrun.it. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Runrun.it. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Runrun.it. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Runrun.it. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Runrun.it. |

