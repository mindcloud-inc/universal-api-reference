# Logo.dev: Native API Reference

A consolidated summary of Logo.dev's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.logo.dev/docs
- **API base URL:** `https://api.logo.dev`

## Authentication

### API Key Pair

Use a publishable key for img.logo.dev and a secret key for api.logo.dev.

### Credentials

- **API Key:** `apiKey` · required
- **Publishable Key:** `publishableKey` · required · Publishable key (pk_) used for img.logo.dev requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.logo.dev/docs/platform/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Describe Company](actions/describe-company.md) | `GET /describe/:domain` | [docs](https://www.logo.dev/docs/describe/introduction) |
| [Get Company Logo by Domain](actions/get-company-logo-by-domain.md) | `GET https://img.logo.dev/:domain` | [docs](https://www.logo.dev/docs/logo-images/domain-logos) |
| [Search Company Domains](actions/search-company-domains.md) | `GET /search` | [docs](https://www.logo.dev/docs/brand-search/introduction) |
