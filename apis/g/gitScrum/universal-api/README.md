# <img src="https://images.mindcloud.co/apps/icons/git-scrum_1775084066120.png" alt="GitScrum logo" width="28" height="28"> GitScrum: Universal API

GitScrum is a project management platform for developers and remote teams that exposes workspaces, projects, tasks, sprints, comments, wiki, discussions, notes, clients, invoices, and analytics through a bearer-token REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gitScrum/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gitscrum.com
- **Vendor API docs:** https://docs.gitscrum.com/en/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Authentication](actions/verify-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Refresh Token](actions/refresh-token.md) | GET | Retrieves a refreshed access token from GitScrum. |

### Backlog Items

| Action | Method | Description |
| --- | --- | --- |
| [Get User Story](actions/get-user-story.md) | GET | Retrieves a specific GitScrum user story. |
| [List User Stories](actions/list-user-stories.md) | GET | Retrieves a list of GitScrum user stories. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves a list of GitScrum workflows. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves a list of GitScrum comments. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves details for a specific GitScrum workspace. |
| [Get Workspace Stats](actions/get-workspace-stats.md) | GET | Retrieves statistics for the current GitScrum workspace. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves a list of GitScrum workspaces. |
| [Verify Authentication](actions/verify-authentication.md) | GET | Retrieves the authenticated GitScrum account details. |

### Epics

| Action | Method | Description |
| --- | --- | --- |
| [List Epics](actions/list-epics.md) | GET | Retrieves a list of GitScrum epics. |

### Estimates

| Action | Method | Description |
| --- | --- | --- |
| [List Effort Levels](actions/list-effort-levels.md) | GET | Retrieves available effort levels from GitScrum. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves a list of GitScrum labels. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get My Workspace Role](actions/get-my-workspace-role.md) | GET | Retrieves your role in a GitScrum workspace. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves members of a GitScrum project. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves details for a specific GitScrum project. |
| [Get Project Stats](actions/get-project-stats.md) | GET | Retrieves statistics for a specific GitScrum project. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of GitScrum projects. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds matching records in GitScrum by search query. |

### Sprints

| Action | Method | Description |
| --- | --- | --- |
| [Get Sprint](actions/get-sprint.md) | GET | Retrieves details for a specific GitScrum sprint. |
| [Get Sprint KPIs](actions/get-sprint-kpis.md) | GET | Retrieves KPI metrics for a GitScrum sprint. |
| [Get Sprint Stats](actions/get-sprint-stats.md) | GET | Retrieves statistics for a GitScrum sprint. |
| [List Sprints](actions/list-sprints.md) | GET | Retrieves a list of GitScrum sprints. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves details for a specific GitScrum task. |
| [Get Task by Code](actions/get-task-by-code.md) | GET | Retrieves a GitScrum task by code. |
| [List My Tasks](actions/list-my-tasks.md) | GET | Retrieves your tasks across GitScrum workspaces. |
| [List Task Types](actions/list-task-types.md) | GET | Retrieves available task types from GitScrum. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of GitScrum tasks. |
| [List Today's Tasks](actions/list-todays-tasks.md) | GET | Retrieves your GitScrum tasks for today. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Available Project Users](actions/list-available-project-users.md) | GET | Retrieves available users for a GitScrum project. |
| [List Project Assignees](actions/list-project-assignees.md) | GET | Retrieves assignees for a GitScrum project. |

