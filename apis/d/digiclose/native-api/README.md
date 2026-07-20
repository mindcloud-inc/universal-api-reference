# Digiclose: Native API Reference

A consolidated summary of Digiclose's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.digiclose.ai/api-documentation
- **OpenAPI specification:** https://app.digiclose.ai/api-docs/openapi.json
- **API base URL:** `https://app.digiclose.ai/api/v1`

## Authentication

### API Key

Authenticate Digiclose requests with your Digiclose API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://app.digiclose.ai/api/v1/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Create Task Category](actions/create-task-category.md) | `POST /tasks/categories` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Contact Field Definitions](actions/get-contact-field-definitions.md) | `GET /contacts/fieldset` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /pipelines/:pipeline_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Product](actions/get-product.md) | `GET /products/:product_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Task](actions/get-task.md) | `GET /tasks/:task_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Get Team](actions/get-team.md) | `GET /teams/:team_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Contact Notices](actions/list-contact-notices.md) | `GET /contacts/:contact_id/notices` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Contact Tasks](actions/list-contact-tasks.md) | `GET /contacts/:contact_id/tasks` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Pipeline Deal Phases](actions/list-pipeline-deal-phases.md) | `GET /pipelines/:pipeline_id/deal-phases` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Recent Products](actions/list-recent-products.md) | `GET /products/recent` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Recent Tasks](actions/list-recent-tasks.md) | `GET /tasks/recent` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Task Categories](actions/list-task-categories.md) | `GET /tasks/categories` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://app.digiclose.ai/api/v1/docs) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://app.digiclose.ai/api/v1/docs) |
