# Responsr: Native API Reference

A consolidated summary of Responsr's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://app.responsr.io/docs
- **OpenAPI specification:** https://app.responsr.io/docs/v1/responsrapi.json
- **API base URL:** `https://app.responsr.io`

## Authentication

### Bearer Token

Use a Responsr personal or tenant access token as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.responsr.io/docs)

## Pagination

Use `PageSize` in the query string to set the page size (default 10; accepted range 1–200). Use `Page` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | `GET /api/v1.0/personalaccesstokens/:id` | [docs](https://app.responsr.io/docs) |
| [Get Async Task](actions/get-async-task.md) | `GET /api/v1.0/asynctasks/:id` | [docs](https://app.responsr.io/docs) |
| [Get Default Access Token](actions/get-default-access-token.md) | `GET /api/v1.0/personalaccesstokens/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Language](actions/get-default-language.md) | `GET /api/v1.0/languages/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Person](actions/get-default-person.md) | `GET /api/v1.0/persons/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Project](actions/get-default-project.md) | `GET /api/v1.0/projects/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Project Survey](actions/get-default-project-survey.md) | `GET /api/v1.0/projects/:projectId/surveys/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Project Variable](actions/get-default-project-variable.md) | `GET /api/v1.0/projects/:projectId/variables/default` | [docs](https://app.responsr.io/docs) |
| [Get Default Project Webhook](actions/get-default-project-webhook.md) | `GET /api/v1.0/projects/:projectId/webhooks/default` | [docs](https://app.responsr.io/docs) |
| [Get Default User](actions/get-default-user.md) | `GET /api/v1.0/users/default` | [docs](https://app.responsr.io/docs) |
| [Get Default User Group](actions/get-default-user-group.md) | `GET /api/v1.0/usergroups/default` | [docs](https://app.responsr.io/docs) |
| [Get Language](actions/get-language.md) | `GET /api/v1.0/languages/:id` | [docs](https://app.responsr.io/docs) |
| [Get Person](actions/get-person.md) | `GET /api/v1.0/persons/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project](actions/get-project.md) | `GET /api/v1.0/projects/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Case](actions/get-project-case.md) | `GET /api/v1.0/projects/:projectId/cases/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Dashboard](actions/get-project-dashboard.md) | `GET /api/v1.0/projects/:projectId/dashboards/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Notification](actions/get-project-notification.md) | `GET /api/v1.0/projects/:projectId/notifications/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Result](actions/get-project-result.md) | `GET /api/v1.0/projects/:projectId/results/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Survey](actions/get-project-survey.md) | `GET /api/v1.0/projects/:projectId/surveys/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Variable](actions/get-project-variable.md) | `GET /api/v1.0/projects/:projectId/variables/:id` | [docs](https://app.responsr.io/docs) |
| [Get Project Webhook](actions/get-project-webhook.md) | `GET /api/v1.0/projects/:projectId/webhooks/:id` | [docs](https://app.responsr.io/docs) |
| [Get User](actions/get-user.md) | `GET /api/v1.0/users/:id` | [docs](https://app.responsr.io/docs) |
| [Get User Group](actions/get-user-group.md) | `GET /api/v1.0/usergroups/:id` | [docs](https://app.responsr.io/docs) |
| [List Access Tokens](actions/list-access-tokens.md) | `GET /api/v1.0/personalaccesstokens` | [docs](https://app.responsr.io/docs) |
| [List Async Tasks](actions/list-async-tasks.md) | `GET /api/v1.0/asynctasks` | [docs](https://app.responsr.io/docs) |
| [List Languages](actions/list-languages.md) | `GET /api/v1.0/languages` | [docs](https://app.responsr.io/docs) |
| [List Notifications](actions/list-notifications.md) | `GET /api/v1.0/notifications` | [docs](https://app.responsr.io/docs) |
| [List Persons](actions/list-persons.md) | `GET /api/v1.0/persons` | [docs](https://app.responsr.io/docs) |
| [List Project Cases](actions/list-project-cases.md) | `GET /api/v1.0/projects/:projectId/cases` | [docs](https://app.responsr.io/docs) |
| [List Project Dashboards](actions/list-project-dashboards.md) | `GET /api/v1.0/projects/:projectId/dashboards` | [docs](https://app.responsr.io/docs) |
| [List Project Notifications](actions/list-project-notifications.md) | `GET /api/v1.0/projects/:projectId/notifications` | [docs](https://app.responsr.io/docs) |
| [List Project Results](actions/list-project-results.md) | `GET /api/v1.0/projects/:projectId/results` | [docs](https://app.responsr.io/docs) |
| [List Project Surveys](actions/list-project-surveys.md) | `GET /api/v1.0/projects/:projectId/surveys` | [docs](https://app.responsr.io/docs) |
| [List Project Users](actions/list-project-users.md) | `GET /api/v1.0/projects/:projectId/users` | [docs](https://app.responsr.io/docs) |
| [List Project Variables](actions/list-project-variables.md) | `GET /api/v1.0/projects/:projectId/variables` | [docs](https://app.responsr.io/docs) |
| [List Project Webhooks](actions/list-project-webhooks.md) | `GET /api/v1.0/projects/:projectId/webhooks` | [docs](https://app.responsr.io/docs) |
| [List Projects](actions/list-projects.md) | `GET /api/v1.0/projects` | [docs](https://app.responsr.io/docs) |
| [List User Groups](actions/list-user-groups.md) | `GET /api/v1.0/usergroups` | [docs](https://app.responsr.io/docs) |
| [List Users](actions/list-users.md) | `GET /api/v1.0/users` | [docs](https://app.responsr.io/docs) |
| [List Variables](actions/list-variables.md) | `GET /api/v1.0/variables` | [docs](https://app.responsr.io/docs) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /api/v1.0/webhooks/events` | [docs](https://app.responsr.io/docs) |
