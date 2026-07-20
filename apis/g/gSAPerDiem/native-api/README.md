# GSA Per Diem: Native API Reference

A consolidated summary of GSA Per Diem's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://open.gsa.gov/api/perdiem/
- **OpenAPI specification:** https://open.gsa.gov/api/perdiem/v2/openapi.yaml
- **API base URL:** `https://api.gsa.gov/travel/perdiem/v2`

## Authentication

### API Key

api.data.gov API key for the GSA Per Diem API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://open.gsa.gov/api/perdiem/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Per Diem Rates by City](actions/get-per-diem-rates-by-city.md) | `GET /rates/city/:city/state/:state/year/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
| [Get Per Diem Rates by ZIP Code](actions/get-per-diem-rates-by-zip-code.md) | `GET /rates/zip/:zip/year/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
| [List CONUS Lodging Rates](actions/list-conus-lodging-rates.md) | `GET /rates/conus/lodging/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
| [List CONUS M&IE Breakdown Rates](actions/list-conus-mie-breakdown-rates.md) | `GET /rates/conus/mie/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
| [List CONUS ZIP Code Destination IDs](actions/list-conus-zip-code-destination-ids.md) | `GET /rates/conus/zipcodes/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
| [List Per Diem Rates by State](actions/list-per-diem-rates-by-state.md) | `GET /rates/state/:state/year/:year` | [docs](https://open.gsa.gov/api/perdiem/) |
