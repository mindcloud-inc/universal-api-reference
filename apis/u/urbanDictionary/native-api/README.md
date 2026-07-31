# Urban Dictionary: Native API Reference

A consolidated summary of Urban Dictionary's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.urbandictionary.com/v0/define
- **API base URL:** `https://api.urbandictionary.com`

## Authentication

### Public API

Urban Dictionary's official API endpoint does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://api.urbandictionary.com/v0/define)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `list`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Look Up Definitions](actions/look-up-definitions.md) | `GET /v0/define` | [docs](https://api.urbandictionary.com/v0/define) |
