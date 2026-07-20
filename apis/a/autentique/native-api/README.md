# Autentique: Native API Reference

A consolidated summary of Autentique's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.autentique.com.br/api
- **API base URL:** `https://api.autentique.com.br/v2/graphql`

## Authentication

### API Key

Autentique API token generated in the Autentique dashboard and sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.autentique.com.br/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Current User](actions/fetch-current-user.md) | `POST` | [docs](https://docs.autentique.com.br/api/queries/fetch-current-user) |
| [Get Current Organization](actions/get-current-organization.md) | `POST` | [docs](https://docs.autentique.com.br/api/queries/listing-organizations) |
| [List Folders](actions/list-folders.md) | `POST` | [docs](https://docs.autentique.com.br/api/queries/listing-folders) |
| [List Organizations](actions/list-organizations.md) | `POST` | [docs](https://docs.autentique.com.br/api/queries/listing-organizations) |
