# Realtor.com: Native API Reference

A consolidated summary of Realtor.com's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.listhub.com/api-documentation/
- **OpenAPI specification:** https://api.listhub.com/api/swagger/index.html
- **API base URL:** `https://api.listhub.com`

## Authentication

### OAuth2 Client Credentials

ListHub OAuth2 client-credentials authentication for publisher API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.listhub.com/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://www.listhub.com/api-documentation/)

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–500).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Metadata](actions/get-metadata.md) | `GET /odata/$metadata` | [docs](https://www.listhub.com/api-documentation/) |
| [Get Property](actions/get-property.md) | `GET /odata/Property('{{listingKey}}')` | [docs](https://www.listhub.com/api-documentation/) |
| [List Properties](actions/list-properties.md) | `GET /odata/Property` | [docs](https://www.listhub.com/api-documentation/) |
| [Sync Properties](actions/sync-properties.md) | `GET /odata/Sync` | [docs](https://www.listhub.com/api-documentation/) |
