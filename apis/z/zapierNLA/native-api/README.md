# Zapier NLA: Native API Reference

A consolidated summary of Zapier NLA's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://nla.zapier.com/api/v1/docs
- **OpenAPI specification:** https://nla.zapier.com/api/v1/dynamic/openapi.json
- **API base URL:** `https://actions.zapier.com`

## Authentication

### Zapier NLA API Key

Zapier NLA server-side authentication. Requests send the credential in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Zapier NLA API key. The API configuration sends this value as the x-api-key header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://nla.zapier.com/api/v1/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | `GET /api/v1/check/` | [docs](https://nla.zapier.com/api/v1/docs) |
| [Execute Dynamic Exposed Action](actions/execute-dynamic-exposed-action.md) | `POST /api/v1/dynamic/exposed/:exposed_app_action_id/execute/` | [docs](https://nla.zapier.com/api/v1/docs) |
| [Execute Exposed Action](actions/execute-exposed-action.md) | `POST /api/v1/exposed/:exposed_app_action_id/execute/` | [docs](https://nla.zapier.com/api/v1/docs) |
| [Get Configuration Link](actions/get-configuration-link.md) | `GET /api/v1/configuration-link/` | [docs](https://nla.zapier.com/api/v1/dynamic/docs) |
| [Get Execution Log](actions/get-execution-log.md) | `GET /api/v1/execution-log/:execution_log_id/` | [docs](https://nla.zapier.com/api/v1/dynamic/docs) |
| [List Directory Actions](actions/list-directory-actions.md) | `GET /api/v1/search/actions/` | [docs](https://nla.zapier.com/api/v1/dynamic/docs) |
| [List Exposed Actions](actions/list-exposed-actions.md) | `GET /api/v1/exposed/` | [docs](https://nla.zapier.com/api/v1/dynamic/docs) |
| [List Guided Recipes](actions/list-guided-recipes.md) | `GET /api/v1/search/zaps/` | [docs](https://nla.zapier.com/api/v1/dynamic/docs) |
