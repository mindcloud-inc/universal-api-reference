# MindCloud: Native API Reference

A consolidated summary of MindCloud's API configuration and 3 documented operations.

- **API base URL:** `https://embedded.mindcloud.co/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `data`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST v1/companies` | [docs](https://docs.mindcloud.co) |
| [List Companies](actions/list-companies.md) | `GET v1/companies` | [docs](https://docs.mindcloud.co/) |
| [List Users](actions/list-users.md) | `GET v1/users` |  |
