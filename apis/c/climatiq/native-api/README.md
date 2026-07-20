# Climatiq: Native API Reference

A consolidated summary of Climatiq's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.climatiq.io/docs
- **API base URL:** `https://api.climatiq.io`

## Authentication

### API Key

Authenticate with a Climatiq API key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.climatiq.io/docs/api-reference/authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Estimate Emissions](actions/estimate-emissions.md) | `POST /data/v1/estimate` | [docs](https://www.climatiq.io/docs/api-reference/estimate) |
| [Get Data Versions](actions/get-data-versions.md) | `GET /data/v1/data-versions` | [docs](https://www.climatiq.io/docs/api-reference/data-version-endpoint) |
| [Get Unit Types](actions/get-unit-types.md) | `GET /data/v1/unit-types` | [docs](https://www.climatiq.io/docs/api-reference/unit-types) |
| [Search Emission Factors](actions/search-emission-factors.md) | `GET /data/v1/search` | [docs](https://www.climatiq.io/docs/api-reference/search) |
