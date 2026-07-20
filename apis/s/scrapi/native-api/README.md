# Scrapi: Native API Reference

A consolidated summary of Scrapi's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://scrapi.tech/docs
- **OpenAPI specification:** https://api.scrapi.tech/openapi/v1.json
- **API base URL:** `https://api.scrapi.tech`

## Authentication

### API Key

Authenticate with your ScrAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://scrapi.tech/docs/api_details/v1_scrape)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | `GET /v1/balance` | [docs](https://scrapi.tech/docs/api_details/v1_scrape) |
| [Get Scrape Status](actions/get-scrape-status.md) | `GET /v1/scrape/status/{reference}` | [docs](https://scrapi.tech/docs/api_details/v1_scrape) |
| [List Countries](actions/list-countries.md) | `GET /v1/countries` | [docs](https://scrapi.tech/docs/api_details/v1_scrape) |
| [List Country Cities](actions/list-country-cities.md) | `GET /v1/countries/{countryKey}/cities` | [docs](https://scrapi.tech/docs/api_details/v1_scrape) |
| [Scrape Website](actions/scrape-website.md) | `POST /v1/scrape` | [docs](https://scrapi.tech/docs/api_details/v1_scrape) |
