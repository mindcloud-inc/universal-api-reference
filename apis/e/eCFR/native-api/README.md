# eCFR: Native API Reference

A consolidated summary of eCFR's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://www.ecfr.gov/developers/documentation/api/v1
- **API base URL:** `https://www.ecfr.gov`

## Authentication

### No authentication

The official eCFR API is publicly accessible and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.ecfr.gov/developers/documentation/api/v1)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Search Results](actions/count-search-results.md) | `GET /api/search/v1/count` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Daily Search Counts](actions/get-daily-search-counts.md) | `GET /api/search/v1/counts/daily` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Full Title XML](actions/get-full-title-xml.md) | `GET /api/versioner/v1/full/:date/title-:title.xml` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Hierarchy Search Counts](actions/get-hierarchy-search-counts.md) | `GET /api/search/v1/counts/hierarchy` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Search Suggestions](actions/get-search-suggestions.md) | `GET /api/search/v1/suggestions` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Title Ancestry](actions/get-title-ancestry.md) | `GET /api/versioner/v1/ancestry/:date/title-:title.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Title Search Counts](actions/get-title-search-counts.md) | `GET /api/search/v1/counts/titles` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Get Title Structure](actions/get-title-structure.md) | `GET /api/versioner/v1/structure/:date/title-:title.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [List Agencies](actions/list-agencies.md) | `GET /api/admin/v1/agencies.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [List Corrections](actions/list-corrections.md) | `GET /api/admin/v1/corrections.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [List Imported Titles](actions/list-imported-titles.md) | `GET /api/versioner-import/v1/titles` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [List Title Versions](actions/list-title-versions.md) | `GET /api/versioner/v1/versions/title-:title.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [List Titles](actions/list-titles.md) | `GET /api/versioner/v1/titles.json` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Search Regulations](actions/search-regulations.md) | `GET /api/search/v1/results` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
| [Summarize Search Results](actions/summarize-search-results.md) | `GET /api/search/v1/summary` | [docs](https://www.ecfr.gov/developers/documentation/api/v1) |
