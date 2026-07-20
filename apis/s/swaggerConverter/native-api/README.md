# Swagger Converter: Native API Reference

A consolidated summary of Swagger Converter's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://converter.swagger.io/
- **OpenAPI specification:** https://converter.swagger.io/api/openapi.json
- **API base URL:** `https://converter.swagger.io/api/`

## Authentication

### No authentication

Swagger Converter is a public API and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://converter.swagger.io/api/openapi.json)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Definition by Content](actions/convert-definition-by-content.md) | `POST convert` | [docs](https://converter.swagger.io/api/openapi.json) |
| [Convert Definition by URL](actions/convert-definition-by-url.md) | `GET convert` | [docs](https://converter.swagger.io/api/openapi.json) |
