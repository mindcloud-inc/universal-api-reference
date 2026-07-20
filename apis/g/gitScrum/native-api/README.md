# GitScrum: Native API Reference

A consolidated summary of GitScrum's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.gitscrum.com/en/api/
- **API base URL:** `https://services.gitscrum.com`

## Authentication

### Bearer Token

Authenticate with a GitScrum bearer access token issued by the login endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gitscrum.com/en/api/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get My Workspace Role](actions/get-my-workspace-role.md) | `GET /companies/:slug/my-role` | [docs](https://docs.gitscrum.com/en/api/workspaces) |
| [Get Project](actions/get-project.md) | `GET /projects/:slug` | [docs](https://docs.gitscrum.com/en/api/projects) |
| [Get Project Stats](actions/get-project-stats.md) | `GET /projects/:slug/stats` | [docs](https://docs.gitscrum.com/en/api/projects) |
| [Get Sprint](actions/get-sprint.md) | `GET /sprints/:slug` | [docs](https://docs.gitscrum.com/en/api/sprints) |
| [Get Sprint KPIs](actions/get-sprint-kpis.md) | `GET /sprints/:slug/kpis` | [docs](https://docs.gitscrum.com/en/api/sprints) |
| [Get Sprint Stats](actions/get-sprint-stats.md) | `GET /sprints/:slug/stats` | [docs](https://docs.gitscrum.com/en/api/sprints) |
| [Get Task](actions/get-task.md) | `GET /tasks/:uuid` | [docs](https://docs.gitscrum.com/en/api/tasks) |
| [Get Task by Code](actions/get-task-by-code.md) | `GET /tasks/by-code/:code` | [docs](https://docs.gitscrum.com/en/api/tasks) |
| [Get User Story](actions/get-user-story.md) | `GET /user-stories/:slug` | [docs](https://docs.gitscrum.com/en/api/user-stories) |
| [Get Workspace](actions/get-workspace.md) | `GET /companies/:slug` | [docs](https://docs.gitscrum.com/en/api/workspaces) |
| [Get Workspace Stats](actions/get-workspace-stats.md) | `GET /companies/stats` | [docs](https://docs.gitscrum.com/en/api/workspaces) |
| [List Available Project Users](actions/list-available-project-users.md) | `GET /project-members/:projectSlug/available-users` | [docs](https://docs.gitscrum.com/en/api/project-members) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://docs.gitscrum.com/en/api/comments) |
| [List Effort Levels](actions/list-effort-levels.md) | `GET /project-templates/effort` | [docs](https://docs.gitscrum.com/en/api/task-types) |
| [List Epics](actions/list-epics.md) | `GET /user-story-epics` | [docs](https://docs.gitscrum.com/en/api/epics) |
| [List Labels](actions/list-labels.md) | `GET /projects-labels` | [docs](https://docs.gitscrum.com/en/api/labels) |
| [List My Tasks](actions/list-my-tasks.md) | `GET /tasks/all-workspaces` | [docs](https://docs.gitscrum.com/en/api/tasks) |
| [List Project Assignees](actions/list-project-assignees.md) | `GET /project-members/:projectSlug/assignees` | [docs](https://docs.gitscrum.com/en/api/project-members) |
| [List Project Members](actions/list-project-members.md) | `GET /project-members/:projectSlug/members` | [docs](https://docs.gitscrum.com/en/api/project-members) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.gitscrum.com/en/api/projects) |
| [List Sprints](actions/list-sprints.md) | `GET /sprints` | [docs](https://docs.gitscrum.com/en/api/sprints) |
| [List Task Types](actions/list-task-types.md) | `GET /project-templates/type` | [docs](https://docs.gitscrum.com/en/api/task-types) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://docs.gitscrum.com/en/api/tasks) |
| [List Today's Tasks](actions/list-todays-tasks.md) | `GET /tasks/my-today` | [docs](https://docs.gitscrum.com/en/api/tasks) |
| [List User Stories](actions/list-user-stories.md) | `GET /user-stories` | [docs](https://docs.gitscrum.com/en/api/user-stories) |
| [List Workflows](actions/list-workflows.md) | `GET /projects-workflows` | [docs](https://docs.gitscrum.com/en/api/workflows) |
| [List Workspaces](actions/list-workspaces.md) | `GET /companies` | [docs](https://docs.gitscrum.com/en/api/workspaces) |
| [Refresh Token](actions/refresh-token.md) | `POST /auth/refresh` | [docs](https://docs.gitscrum.com/en/api/authentication) |
| [Search](actions/search.md) | `GET /search` | [docs](https://docs.gitscrum.com/en/api/search) |
| [Verify Authentication](actions/verify-authentication.md) | `POST /auth/me` | [docs](https://docs.gitscrum.com/en/api/authentication) |
