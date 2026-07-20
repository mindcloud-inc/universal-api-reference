# Finnish BIS: Native API Reference

A consolidated summary of Finnish BIS's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en
- **OpenAPI specification:** https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en
- **API base URL:** `https://avoindata.prh.fi/opendata-ytj-api/v3`

## Authentication

### No authentication

The official PRH OpenData YTJ API exposes public endpoints with no documented authentication or security scheme.

This API does not require request authentication.

[Official authentication documentation](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Code List Description](actions/get-code-list-description.md) | `GET /description` | [docs](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en) |
| [List Post Codes](actions/list-post-codes.md) | `GET /post_codes` | [docs](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en) |
| [Search Companies](actions/search-companies.md) | `GET /companies` | [docs](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en) |
