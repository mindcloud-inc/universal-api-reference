# Zillow Econ: Native API Reference

A consolidated summary of Zillow Econ's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://bridgedataoutput.com/docs/platform
- **API base URL:** `https://api.bridgedataoutput.com/api/v2`

## Authentication

### Bridge server token

Bridge server token used as the access_token value for Bridge-hosted Zillow Economic Data requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bridgedataoutput.com/docs/platform)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get market report](actions/get-market-report.md) | `GET /zgecon/marketreport` | [docs](https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data) |
| [Get market type metadata](actions/get-market-type-metadata.md) | `GET /zgecon/type` | [docs](https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data) |
| [Get region metadata](actions/get-region-metadata.md) | `GET /zgecon/region` | [docs](https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data) |
