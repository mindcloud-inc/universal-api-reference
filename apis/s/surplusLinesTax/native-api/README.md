# Surplus Lines Tax: Native API Reference

A consolidated summary of Surplus Lines Tax's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://surpluslinesapi.com/docs/
- **OpenAPI specification:** https://surpluslinesapi.com/docs/openapi/surpluslines-openapi.yaml
- **API base URL:** `https://api.surpluslinesapi.com/v1`

## Authentication

### API Key

Use an API key generated in the Surplus Lines Tax dashboard and sent in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://surpluslinesapi.com/docs/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Surplus Lines Taxes](actions/calculate-surplus-lines-taxes.md) | `POST /calculate` | [docs](https://surpluslinesapi.com/docs/#calculate) |
| [Retrieve Historical Surplus Lines Tax Rates](actions/retrieve-historical-surplus-lines-tax-rates.md) | `GET /historical-rates` | [docs](https://surpluslinesapi.com/docs/#historical-rates) |
