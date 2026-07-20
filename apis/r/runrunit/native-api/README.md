# Runrun.it: Native API Reference

A consolidated summary of Runrun.it's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://runrun.it/api/documentation
- **API base URL:** `https://runrun.it/api/v1.0`

## Authentication

### App-Key + User-Token

### Credentials

- **App Key:** `appKey` · required · Runrun.it App-Key header value.
- **User Token:** `userToken` · required · Runrun.it User-Token header value.

Send these headers with each API request:

```http
App-Key: <appKey>
User-Token: <userToken>
```

[Official authentication documentation](https://runrun.it/api/documentation#how-to-authenticate-to-use-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Team](actions/add-user-to-team.md) | `POST /teams/:id/add_member` | [docs](https://runrun.it/api/documentation#teams-add-a-user-to-a-team) |
| [Change Project Board Stage](actions/change-project-board-stage.md) | `POST /projects/:id/change_board_stage` | [docs](https://runrun.it/api/documentation#projects-change-a-project-board-stage) |
| [Clone Project](actions/clone-project.md) | `POST /projects/:id/clone` | [docs](https://runrun.it/api/documentation#projects-clone-a-project) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://runrun.it/api/documentation#clients-create-a-client) |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://runrun.it/api/documentation#comments-create-a-new-comment) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://runrun.it/api/documentation#projects-create-a-project) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://runrun.it/api/documentation#tasks-create-a-task) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://runrun.it/api/documentation#teams-create-a-team) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://runrun.it/api/documentation#users-create-a-user) |
| [Deliver Task](actions/deliver-task.md) | `POST /tasks/:id/deliver` | [docs](https://runrun.it/api/documentation#tasks-deliver-a-task) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://runrun.it/api/documentation#clients-show-a-client) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://runrun.it/api/documentation#projects-show-a-project) |
| [Get Project Group](actions/get-project-group.md) | `GET /clients/:client_id/project_groups/:id` | [docs](https://runrun.it/api/documentation#project-groups-show-a-project-group) |
| [Get Project Sub Group](actions/get-project-sub-group.md) | `GET /project_groups/:project_group_id/project_sub_groups/:id` | [docs](https://runrun.it/api/documentation#project-sub-groups-show-a-project-sub-group) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://runrun.it/api/documentation#tasks-show-a-task) |
| [Get Task Type](actions/get-task-type.md) | `GET /task_types/:id` | [docs](https://runrun.it/api/documentation#tasktype-show-a-task-type) |
| [Get Team](actions/get-team.md) | `GET /teams/:id` | [docs](https://runrun.it/api/documentation#teams-show-a-team) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://runrun.it/api/documentation#users-get-a-user-by-id) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://runrun.it/api/documentation#activities-get-activities) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://runrun.it/api/documentation#clients-list-clients) |
| [List Project Groups](actions/list-project-groups.md) | `GET /clients/:client_id/project_groups` | [docs](https://runrun.it/api/documentation#project-groups-list-all-project-groups) |
| [List Project Sub Groups](actions/list-project-sub-groups.md) | `GET /project_groups/:project_group_id/project_sub_groups` | [docs](https://runrun.it/api/documentation#project-sub-groups-list-all-project-sub-groups-using-project-group-id) |
| [List Project Users](actions/list-project-users.md) | `GET /projects/:id/related_users` | [docs](https://runrun.it/api/documentation#projects-list-users-related-in-a-project) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://runrun.it/api/documentation#projects-list-all-projects) |
| [List Task Comments](actions/list-task-comments.md) | `GET /tasks/:task_id/comments` | [docs](https://runrun.it/api/documentation#comments-list-comments-on-a-task) |
| [List Task Subtasks](actions/list-task-subtasks.md) | `GET /tasks/:id/subtasks` | [docs](https://runrun.it/api/documentation#tasks-show-task-subtasks) |
| [List Task Types](actions/list-task-types.md) | `GET /task_types` | [docs](https://runrun.it/api/documentation#tasktype-list-task-types) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://runrun.it/api/documentation#teams-list-teams) |
| [List Time Worked](actions/list-time-worked.md) | `GET /reports/time_worked` | [docs](https://runrun.it/api/documentation#time-worked-list-all-time-worked-grouped-and-filtered-by-parameters) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://runrun.it/api/documentation#users-list-all-users) |
| [Move Task To Project](actions/move-task-to-project.md) | `POST /tasks/:id/change_project` | [docs](https://runrun.it/api/documentation#tasks-change-the-project-from-task-to-another) |
| [Pause Task](actions/pause-task.md) | `POST /tasks/:id/pause` | [docs](https://runrun.it/api/documentation#tasks-pause-a-task) |
| [Remove User From Team](actions/remove-user-from-team.md) | `POST /teams/:id/remove_member` | [docs](https://runrun.it/api/documentation#teams-remove-a-user-from-team) |
| [Reopen Task](actions/reopen-task.md) | `POST /tasks/:id/reopen` | [docs](https://runrun.it/api/documentation#tasks-reopen-a-task) |
| [Search Tags](actions/search-tags.md) | `GET /tags` | [docs](https://runrun.it/api/documentation#tags-query-tags) |
| [Search Tasks](actions/search-tasks.md) | `GET /tasks` | [docs](https://runrun.it/api/documentation#tasks-query-tasks) |
| [Start Task](actions/start-task.md) | `POST /tasks/:id/play` | [docs](https://runrun.it/api/documentation#tasks-play-a-task) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://runrun.it/api/documentation#clients-update-a-client) |
| [Update Team](actions/update-team.md) | `PUT /teams/:id` | [docs](https://runrun.it/api/documentation#teams-update-a-team) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://runrun.it/api/documentation#users-update-a-user) |
