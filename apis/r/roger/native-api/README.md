# Roger: Native API Reference

A consolidated summary of Roger's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developer.rogerroger.io
- **OpenAPI specification:** https://api.rogerroger.io/docs.jsonopenapi
- **API base URL:** `https://api.rogerroger.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.rogerroger.io/getting-started/authentication-setup)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json, application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `itemsPerPage` in the query string to set the page size (default 15; accepted range 0–30). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://developer.rogerroger.io/organizations) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://developer.rogerroger.io/crm/people) |
| [Create Segment](actions/create-segment.md) | `POST /segments` | [docs](https://developer.rogerroger.io/lists) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developer.rogerroger.io/global/tags) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developer.rogerroger.io/tasks) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developer.rogerroger.io/webhooks/set-up-a-webhook) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /organizations/:id` | [docs](https://developer.rogerroger.io/organizations) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/:id` | [docs](https://developer.rogerroger.io/crm/people) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:id` | [docs](https://developer.rogerroger.io/lists) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://developer.rogerroger.io/tasks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developer.rogerroger.io/webhooks/set-up-a-webhook) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:id` | [docs](https://developer.rogerroger.io/organizations) |
| [Get Person](actions/get-person.md) | `GET /people/:id` | [docs](https://developer.rogerroger.io/crm/people) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:id` | [docs](https://developer.rogerroger.io/lists) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:id` | [docs](https://developer.rogerroger.io/global/tags) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://developer.rogerroger.io/tasks) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://developer.rogerroger.io/webhooks/set-up-a-webhook) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:id` | [docs](https://developer.rogerroger.io/workspaces/workspaces) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developer.rogerroger.io/organizations) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://developer.rogerroger.io/crm/people) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://developer.rogerroger.io/lists) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.rogerroger.io/global/tags) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developer.rogerroger.io/tasks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developer.rogerroger.io/webhooks/set-up-a-webhook) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://developer.rogerroger.io/workspaces/workspaces) |
| [Update Organization](actions/update-organization.md) | `PATCH /organizations/:id` | [docs](https://developer.rogerroger.io/organizations) |
| [Update Person](actions/update-person.md) | `PATCH /people/:id` | [docs](https://developer.rogerroger.io/crm/people) |
| [Update Segment](actions/update-segment.md) | `PATCH /segments/:id` | [docs](https://developer.rogerroger.io/lists) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/:id` | [docs](https://developer.rogerroger.io/global/tags) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://developer.rogerroger.io/tasks) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:id` | [docs](https://developer.rogerroger.io/webhooks/set-up-a-webhook) |
