# RD Station CRM: Native API Reference

A consolidated summary of RD Station CRM's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.rdstation.com/reference/crm-v2-introduction
- **API base URL:** `https://api.rd.services/crm/v2`

## Authentication

### OAuth2

OAuth2 authorization code flow for RD Station CRM v2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.rdstation.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.rd.services/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.rd.services/oauth2/token.

[Official authentication documentation](https://developers.rdstation.com/reference/crm-v2-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; minimum 1). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.rdstation.com/reference/crm-v2-create-contact) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://developers.rdstation.com/reference/crm-v2-create-deal) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://developers.rdstation.com/reference/crm-v2-create-organization) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developers.rdstation.com/reference/crm-v2-create-task) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-contact) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-deal) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-organization) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /pipelines/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-pipeline) |
| [Get Pipeline Stage](actions/get-pipeline-stage.md) | `GET /pipelines/:pipeline_id/stages/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-stage-from-pipeline) |
| [Get Source](actions/get-source.md) | `GET /sources/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-source) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-task) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-get-user) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.rdstation.com/reference/crm-v2-list-contacts) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://developers.rdstation.com/reference/crm-v2-list-deals) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developers.rdstation.com/reference/crm-v2-list-organizations) |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | `GET /pipelines/:pipeline_id/stages` | [docs](https://developers.rdstation.com/reference/crm-v2-list-stages-from-pipeline) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://developers.rdstation.com/reference/crm-v2-list-pipelines) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://developers.rdstation.com/reference/crm-v2-list-sources) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developers.rdstation.com/reference/crm-v2-list-tasks) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.rdstation.com/reference/crm-v2-list-users) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-update-contact) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-update-deal) |
| [Update Organization](actions/update-organization.md) | `PUT /organizations/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-update-organization) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://developers.rdstation.com/reference/crm-v2-update-task) |
