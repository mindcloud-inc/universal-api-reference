# Address Labs: Native API Reference

A consolidated summary of Address Labs's API configuration, with links to official documentation.

- **Official docs:** https://github.com/addresslabs/api-docs
- **API base URL:** `http://api.addresslabs.com/v1/`

## Authentication

### No authentication

Address Labs public API endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/addresslabs/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
