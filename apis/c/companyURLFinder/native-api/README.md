# Company URL Finder: Native API Reference

A consolidated summary of Company URL Finder's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.companyurlfinder.com/apis
- **API base URL:** `https://api.companyurlfinder.com`

## Authentication

### API Key

Use your Company URL Finder API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://apidocs.companyurlfinder.com/apis/authentication)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Company Query to LinkedIn URL](actions/company-query-to-linkedin-url.md) | `POST /v2/services/name_to_linkedin` | [docs](https://apidocs.companyurlfinder.com/apis/linkedin-company-url-finder) |
| [Get Company Name by Domain](actions/get-company-name-by-domain.md) | `POST /v2/services/domain_to_name` | [docs](https://apidocs.companyurlfinder.com/apis/company-domain-to-name) |
| [Get Domain by Company Name](actions/get-domain-by-company-name.md) | `POST /v2/services/name_to_domain` | [docs](https://apidocs.companyurlfinder.com/apis/company-name-to-domain) |
