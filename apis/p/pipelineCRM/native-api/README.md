# Pipeline CRM: Native API Reference

A consolidated summary of Pipeline CRM's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.pipelinecrm.com/docs
- **OpenAPI specification:** https://app.pipelinecrm.com/openapi.yaml
- **API base URL:** `https://api.pipelinecrm.com/api/v3`

## Authentication

### API Key

Connect with a Pipeline app key and user API key.

### Credentials

- **API Key:** `apiKey` · required
- **App Key:** `appKey` · required · Pipeline integration app key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://app.pipelinecrm.com/docs)

## API conventions

Response data is read from `entries`. The total page count is read from `pagination.pages`. The current page number is read from `pagination.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 200; maximum 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /notes` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Create Calendar Entry](actions/create-calendar-entry.md) | `POST /calendar_entries` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Delete Calendar Entry](actions/delete-calendar-entry.md) | `DELETE /calendar_entries/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /deals/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [List Activities](actions/list-activities.md) | `GET /notes` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [List Calendar Entries](actions/list-calendar-entries.md) | `GET /calendar_entries` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Retrieve Activity](actions/retrieve-activity.md) | `GET /notes/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Retrieve Calendar Entry](actions/retrieve-calendar-entry.md) | `GET /calendar_entries/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /companies/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Retrieve Deal](actions/retrieve-deal.md) | `GET /deals/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Retrieve Person](actions/retrieve-person.md) | `GET /people/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Update Activity](actions/update-activity.md) | `PUT /notes/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Update Calendar Entry](actions/update-calendar-entry.md) | `PUT /calendar_entries/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Update Company](actions/update-company.md) | `PUT /companies/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
| [Update Person](actions/update-person.md) | `PUT /people/:id` | [docs](https://app.pipelinecrm.com/openapi.yaml) |
