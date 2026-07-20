# Cloze: Native API Reference

A consolidated summary of Cloze's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.cloze.com/
- **OpenAPI specification:** https://api.cloze.com/api-docs/swagger.json
- **API base URL:** `https://api.cloze.com`

## Authentication

### API Key

Authenticate with a Cloze API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.cloze.com/article/2176-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pagesize` in the query string to set the page size (default 10; accepted range 1–1000). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Communication Record](actions/add-communication-record.md) | `POST /v1/timeline/communication/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-timeline-communication-create/post) |
| [Add Content Record](actions/add-content-record.md) | `POST /v1/timeline/content/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-timeline-content-create/post) |
| [Create Company](actions/create-company.md) | `POST /v1/companies/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-create/post) |
| [Create Person](actions/create-person.md) | `POST /v1/people/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-create/post) |
| [Create Project](actions/create-project.md) | `POST /v1/projects/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-create/post) |
| [Create To Do](actions/create-to-do.md) | `POST /v1/timeline/todo/create` | [docs](https://api.cloze.com/api-docs/#/paths/v1-timeline-todo-create/post) |
| [Delete Company](actions/delete-company.md) | `DELETE /v1/companies/delete` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-delete/delete) |
| [Delete Person](actions/delete-person.md) | `DELETE /v1/people/delete` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-delete/delete) |
| [Delete Project](actions/delete-project.md) | `DELETE /v1/projects/delete` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-delete/delete) |
| [Get Company](actions/get-company.md) | `GET /v1/companies/get` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-get/get) |
| [Get Person](actions/get-person.md) | `GET /v1/people/get` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-get/get) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/get` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-get/get) |
| [Get User Profile](actions/get-user-profile.md) | `GET /v1/user/profile` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-profile/get) |
| [List Contact Segments](actions/list-contact-segments.md) | `GET /v1/user/segments/people` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-segments-people/get) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /v1/user/fields` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-fields/get) |
| [List People And Company Contact Stages](actions/list-people-and-company-contact-stages.md) | `GET /v1/user/stages/people` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-stages-people/get) |
| [List Project Segments](actions/list-project-segments.md) | `GET /v1/user/segments/projects` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-segments-projects/get) |
| [List Project Stages](actions/list-project-stages.md) | `GET /v1/user/stages/projects` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-stages-projects/get) |
| [List Steps](actions/list-steps.md) | `GET /v1/user/steps` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-steps/get) |
| [List Views And Audiences](actions/list-views-and-audiences.md) | `GET /v1/user/views` | [docs](https://api.cloze.com/api-docs/#/paths/v1-user-views/get) |
| [Retrieve Email Opens](actions/retrieve-email-opens.md) | `GET /v1/messages/opens` | [docs](https://api.cloze.com/api-docs/#/paths/v1-messages-opens/get) |
| [Search Companies](actions/search-companies.md) | `GET /v1/companies/find` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-find/get) |
| [Search People](actions/search-people.md) | `GET /v1/people/find` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-find/get) |
| [Search Projects](actions/search-projects.md) | `GET /v1/projects/find` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-find/get) |
| [Stream Companies Feed](actions/stream-companies-feed.md) | `GET /v1/companies/feed` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-feed/get) |
| [Stream People Feed](actions/stream-people-feed.md) | `GET /v1/people/feed` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-feed/get) |
| [Stream Projects Feed](actions/stream-projects-feed.md) | `GET /v1/projects/feed` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-feed/get) |
| [Update Company](actions/update-company.md) | `POST /v1/companies/update` | [docs](https://api.cloze.com/api-docs/#/paths/v1-companies-update/post) |
| [Update Person](actions/update-person.md) | `POST /v1/people/update` | [docs](https://api.cloze.com/api-docs/#/paths/v1-people-update/post) |
| [Update Project](actions/update-project.md) | `POST /v1/projects/update` | [docs](https://api.cloze.com/api-docs/#/paths/v1-projects-update/post) |
