# Freedcamp: Native API Reference

A consolidated summary of Freedcamp's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab
- **API base URL:** `https://freedcamp.com`

## Authentication

### Secured API Key

Uses Freedcamp secured API key authentication (api_key + timestamp + HMAC-SHA1 hash).

### Credentials

- **API Key:** `apiKey` · required · Your Freedcamp API key.
- **API Secret:** `apiSecret` · required · Your Freedcamp secure API secret used to sign each request.

[Official authentication documentation](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /api/v1/comments` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [Create Task](actions/create-task.md) | `POST /api/v1/tasks` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/v1/tasks/:taskId` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/current` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [Get Task](actions/get-task.md) | `GET /api/v1/tasks/:taskId` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [List Milestones](actions/list-milestones.md) | `GET /api/v1/milestones` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [List Notifications](actions/list-notifications.md) | `GET /api/v1/notifications` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/tasks` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [List Time Records](actions/list-time-records.md) | `GET /api/v1/times` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
| [Update Task](actions/update-task.md) | `POST /api/v1/tasks/:taskId` | [docs](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab) |
