# Bureau of Labor Statistics: Native API Reference

A consolidated summary of Bureau of Labor Statistics's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.bls.gov/developers/home.htm
- **API base URL:** `https://api.bls.gov/publicAPI/v2`

## Authentication

### Public API

The selected BLS public read actions do not require credentials. A BLS registration key unlocks higher limits and optional response features, but this draft is configured for unregistered public access.

This API does not require request authentication.

[Official authentication documentation](https://www.bls.gov/developers/home.htm)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Latest Series Data](actions/get-latest-series-data.md) | `GET /timeseries/data/:seriesId` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
| [Get Single Series Data](actions/get-single-series-data.md) | `GET /timeseries/data/:seriesId` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/:surveyAbbreviation` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
| [List Popular Series](actions/list-popular-series.md) | `GET /timeseries/popular` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
| [Query Series Data](actions/query-series-data.md) | `POST /timeseries/data/` | [docs](https://www.bls.gov/developers/api_signature_v2.htm) |
