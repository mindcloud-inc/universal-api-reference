# Twenty: Native API Reference

A consolidated summary of Twenty's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.twenty.com/developers/extend/api
- **API base URL:** `https://api.twenty.com`

## Authentication

### API Key

Authenticate with a Twenty API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.twenty.com/developers/extend/api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pageInfo.endCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 25).

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /rest/companies` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Dashboard](actions/create-dashboard.md) | `POST /rest/dashboards` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Note](actions/create-note.md) | `POST /rest/notes` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Object Metadata](actions/create-object-metadata.md) | `POST /rest/metadata/objects` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /rest/opportunities` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Person](actions/create-person.md) | `POST /rest/people` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Task](actions/create-task.md) | `POST /rest/tasks` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Create Workflow](actions/create-workflow.md) | `POST /rest/workflows` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Company](actions/delete-company.md) | `DELETE /rest/companies/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Dashboard](actions/delete-dashboard.md) | `DELETE /rest/dashboards/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Note](actions/delete-note.md) | `DELETE /rest/notes/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Object Metadata](actions/delete-object-metadata.md) | `DELETE /rest/metadata/objects/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /rest/opportunities/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Person](actions/delete-person.md) | `DELETE /rest/people/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Task](actions/delete-task.md) | `DELETE /rest/tasks/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /rest/workflows/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Company](actions/get-company.md) | `GET /rest/companies/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /rest/dashboards/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Note](actions/get-note.md) | `GET /rest/notes/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Object Metadata](actions/get-object-metadata.md) | `GET /rest/metadata/objects/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /rest/opportunities/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Person](actions/get-person.md) | `GET /rest/people/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Task](actions/get-task.md) | `GET /rest/tasks/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Get Workflow](actions/get-workflow.md) | `GET /rest/workflows/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Companies](actions/list-companies.md) | `GET /rest/companies` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Dashboards](actions/list-dashboards.md) | `GET /rest/dashboards` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Notes](actions/list-notes.md) | `GET /rest/notes` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Object Metadata](actions/list-object-metadata.md) | `GET /rest/metadata/objects` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Opportunities](actions/list-opportunities.md) | `GET /rest/opportunities` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List People](actions/list-people.md) | `GET /rest/people` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Tasks](actions/list-tasks.md) | `GET /rest/tasks` | [docs](https://docs.twenty.com/developers/extend/api) |
| [List Workflows](actions/list-workflows.md) | `GET /rest/workflows` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Company](actions/update-company.md) | `PATCH /rest/companies/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Dashboard](actions/update-dashboard.md) | `PATCH /rest/dashboards/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Note](actions/update-note.md) | `PATCH /rest/notes/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Object Metadata](actions/update-object-metadata.md) | `PATCH /rest/metadata/objects/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /rest/opportunities/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Person](actions/update-person.md) | `PATCH /rest/people/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Task](actions/update-task.md) | `PATCH /rest/tasks/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
| [Update Workflow](actions/update-workflow.md) | `PATCH /rest/workflows/:id` | [docs](https://docs.twenty.com/developers/extend/api) |
