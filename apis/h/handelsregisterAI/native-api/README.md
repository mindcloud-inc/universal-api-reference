# Handelsregister AI: Native API Reference

A consolidated summary of Handelsregister AI's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://handelsregister.ai/en/documentation
- **API base URL:** `https://handelsregister.ai/api/v1`

## Authentication

### API Key

Authenticate with your Handelsregister AI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://handelsregister.ai/en/documentation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create API Token](actions/create-api-token.md) | `POST /auth/tokens/create` | [docs](https://handelsregister.ai/en/documentation) |
| [Download Shareholders List Document](actions/download-shareholders-list-document.md) | `GET /fetch-document` | [docs](https://handelsregister.ai/en/documentation) |
| [Get Company Balance Sheet Accounts](actions/get-company-balance-sheet-accounts.md) | `GET /fetch-organization` | [docs](https://handelsregister.ai/en/documentation) |
| [Get Company Financial KPIs](actions/get-company-financial-kpis.md) | `GET /fetch-organization` | [docs](https://handelsregister.ai/en/documentation) |
| [Get Company Profile](actions/get-company-profile.md) | `GET /fetch-organization` | [docs](https://handelsregister.ai/en/documentation) |
| [Get Company With AI Search](actions/get-company-with-ai-search.md) | `GET /fetch-organization` | [docs](https://handelsregister.ai/en/documentation) |
| [List API Tokens](actions/list-api-tokens.md) | `GET /auth/tokens` | [docs](https://handelsregister.ai/en/documentation) |
| [Revoke API Token](actions/revoke-api-token.md) | `DELETE /auth/tokens/:id` | [docs](https://handelsregister.ai/en/documentation) |
| [Search Organizations](actions/search-organizations.md) | `GET /search-organizations` | [docs](https://handelsregister.ai/en/documentation) |
