# ClinicalTrials.gov: Native API Reference

A consolidated summary of ClinicalTrials.gov's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://clinicaltrials.gov/data-api/api
- **API base URL:** `https://clinicaltrials.gov/api/v2`

## Authentication

### No Authentication

ClinicalTrials.gov API v2 is publicly accessible and does not require credentials for read operations.

This API does not require request authentication.

[Official authentication documentation](https://clinicaltrials.gov/data-api/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | `GET /version` | [docs](https://clinicaltrials.gov/data-api/api) |
| [Get Database Size Statistics](actions/get-database-size-statistics.md) | `GET /stats/size` | [docs](https://clinicaltrials.gov/data-api/api) |
| [Get Enums](actions/get-enums.md) | `GET /studies/enums` | [docs](https://clinicaltrials.gov/data-api/about-api/study-data-structure) |
| [Get Field Size Statistics](actions/get-field-size-statistics.md) | `GET /stats/field/sizes` | [docs](https://clinicaltrials.gov/data-api/about-api/study-data-structure) |
| [Get Field Value Statistics](actions/get-field-value-statistics.md) | `GET /stats/field/values` | [docs](https://clinicaltrials.gov/data-api/about-api/study-data-structure) |
| [Get Search Areas](actions/get-search-areas.md) | `GET /studies/search-areas` | [docs](https://clinicaltrials.gov/data-api/about-api/search-areas) |
| [Get Studies Metadata](actions/get-studies-metadata.md) | `GET /studies/metadata` | [docs](https://clinicaltrials.gov/data-api/api) |
| [Get Study](actions/get-study.md) | `GET /studies/:nctId` | [docs](https://clinicaltrials.gov/data-api/api) |
| [Get Study CSV](actions/get-study-csv.md) | `GET /studies/:nctId` | [docs](https://clinicaltrials.gov/data-api/about-api/csv-download) |
| [Get Study FHIR JSON](actions/get-study-fhir-json.md) | `GET /studies/:nctId` | [docs](https://clinicaltrials.gov/data-api/fhir) |
| [Get Study JSON ZIP](actions/get-study-json-zip.md) | `GET /studies/:nctId` | [docs](https://clinicaltrials.gov/data-api/how-download-study-records) |
| [Get Study RIS](actions/get-study-ris.md) | `GET /studies/:nctId` | [docs](https://clinicaltrials.gov/data-api/about-api/ris-download) |
| [Search Studies](actions/search-studies.md) | `GET /studies` | [docs](https://clinicaltrials.gov/data-api/api) |
| [Search Studies CSV](actions/search-studies-csv.md) | `GET /studies` | [docs](https://clinicaltrials.gov/data-api/about-api/csv-download) |
