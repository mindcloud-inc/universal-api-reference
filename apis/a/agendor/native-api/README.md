# Agendor: Native API Reference

A consolidated summary of Agendor's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://api.agendor.com.br/docs/
- **API base URL:** `https://api.agendor.com.br/v3`

## Authentication

### API Token

Connect with an Agendor user API token. The token is sent as Authorization: Token <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ajuda.agendor.com.br/pt-BR/articles/5482997-o-que-e-e-para-que-usamos-o-token-da-conta)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Deal For Organization](actions/create-deal-for-organization.md) | `POST /organizations/:organization_id/deals` | [docs](https://api.agendor.com.br/docs/#operation/Create%20deal%20for%20organization) |
| [Create Deal For Person](actions/create-deal-for-person.md) | `POST /people/:person_id/deals` | [docs](https://api.agendor.com.br/docs/#operation/Create%20deal%20for%20person) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://api.agendor.com.br/docs/#operation/Create%20organization) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://api.agendor.com.br/docs/#operation/Create%20person) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /organizations/:id` | [docs](https://api.agendor.com.br/docs/#operation/Delete%20organization) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/:id` | [docs](https://api.agendor.com.br/docs/#operation/Delete%20person) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://api.agendor.com.br/docs/#operation/Get%20current%20user) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:id` | [docs](https://api.agendor.com.br/docs/#operation/Get%20organization) |
| [Get Person](actions/get-person.md) | `GET /people/:id` | [docs](https://api.agendor.com.br/docs/#operation/Get%20person) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://api.agendor.com.br/docs/#operation/List%20organizations) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://api.agendor.com.br/docs/#operation/List%20people) |
| [Update Organization](actions/update-organization.md) | `PUT /organizations/:id` | [docs](https://api.agendor.com.br/docs/#operation/Update%20organization) |
| [Update Person](actions/update-person.md) | `PUT /people/:id` | [docs](https://api.agendor.com.br/docs/#operation/Update%20person) |
