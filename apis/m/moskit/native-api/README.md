# Moskit: Native API Reference

A consolidated summary of Moskit's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://moskit.stoplight.io/docs/api-v2/
- **OpenAPI specification:** https://stoplight.io/api/v1/projects/moskit/api-v2/nodes/reference/openapi.yaml?fromExportButton=true&snapshotType=http_service&deref=optimizedBundle
- **API base URL:** `https://api.ms.prod.moskit.services/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://ajuda.moskitcrm.com/pt-BR/articles/1343806-api-publica-para-integracoes)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `quantity` in the query string to set the page size (default 10; accepted range 1–50). Use `start` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST activities` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Create Company](actions/create-company.md) | `POST companies` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Create Contact](actions/create-contact.md) | `POST contacts` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Create Deal](actions/create-deal.md) | `POST deals` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Get Activity](actions/get-activity.md) | `GET activities/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Get Company](actions/get-company.md) | `GET companies/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Get Contact](actions/get-contact.md) | `GET contacts/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Get Deal](actions/get-deal.md) | `GET deals/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Get Project](actions/get-project.md) | `GET projects/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Activities](actions/list-activities.md) | `GET activities` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Companies](actions/list-companies.md) | `GET companies` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Contacts](actions/list-contacts.md) | `GET contacts` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Deals](actions/list-deals.md) | `GET deals` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Projects](actions/list-projects.md) | `GET projects` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Search Activities](actions/search-activities.md) | `POST activities/search` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Search Companies](actions/search-companies.md) | `POST companies/search` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Search Contacts](actions/search-contacts.md) | `POST contacts/search` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Search Deals](actions/search-deals.md) | `POST deals/search` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Search Projects](actions/search-projects.md) | `POST projects/search` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Update Activity](actions/update-activity.md) | `PUT activities/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Update Company](actions/update-company.md) | `PUT companies/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Update Contact](actions/update-contact.md) | `PUT contacts/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Update Deal](actions/update-deal.md) | `PUT deals/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
| [Update Project](actions/update-project.md) | `PUT projects/:id` | [docs](https://moskit.stoplight.io/docs/api-v2/) |
