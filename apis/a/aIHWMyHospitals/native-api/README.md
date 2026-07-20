# AIHW MyHospitals: Native API Reference

A consolidated summary of AIHW MyHospitals's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.aihw.gov.au/reports-data/myhospitals/content/api
- **OpenAPI specification:** https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json
- **API base URL:** `https://myhospitalsapi.aihw.gov.au`

## Authentication

### No authentication

The AIHW MyHospitals API is currently open and free to use and does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://www.aihw.gov.au/reports-data/myhospitals/content/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | `GET /api/v1/datasets/{dataset-id}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [Get Measure](actions/get-measure.md) | `GET /api/v1/measures/{measure-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [Get Reported Measure](actions/get-reported-measure.md) | `GET /api/v1/reported-measures/{reported-measure-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [Get Reported Measure Category](actions/get-reported-measure-category.md) | `GET /api/v1/reported-measure-categories/{reported-measure-category-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [Get Reporting Unit](actions/get-reporting-unit.md) | `GET /api/v1/reporting-units/{reporting-unit-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Bricks Available For Reporting Unit](actions/list-bricks-available-for-reporting-unit.md) | `GET /api/v1/reporting-units/{reporting-unit-code}/bricks-available` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Bricks Available For Reporting Unit Type](actions/list-bricks-available-for-reporting-unit-type.md) | `GET /api/v1/reporting-unit-types/{reporting-unit-type-code}/bricks-available` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Data Items For Dataset](actions/list-data-items-for-dataset.md) | `GET /api/v1/datasets/{dataset-id}/data-items` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Data Items For Measure](actions/list-data-items-for-measure.md) | `GET /api/v1/measures/{measure-code}/data-items` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Data Items For Reported Measure](actions/list-data-items-for-reported-measure.md) | `GET /api/v1/reported-measures/{reported-measure-code}/data-items` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Data Items For Reporting Unit](actions/list-data-items-for-reporting-unit.md) | `GET /api/v1/reporting-units/{reporting-unit-code}/data-items` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Datasets](actions/list-datasets.md) | `GET /api/v1/datasets` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Flat Data Extract](actions/list-flat-data-extract.md) | `GET /api/v1/flat-data-extract/{measure-category-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Flat Formatted Data Extract](actions/list-flat-formatted-data-extract.md) | `GET /api/v1/flat-formatted-data-extract/{measure-category-code}` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Measure Categories](actions/list-measure-categories.md) | `GET /api/v1/measure-categories` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Measures](actions/list-measures.md) | `GET /api/v1/measures` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Measures Available For Reporting Unit](actions/list-measures-available-for-reporting-unit.md) | `GET /api/v1/reporting-units/{reporting-unit-code}/measures-available` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Measures For Measure Category](actions/list-measures-for-measure-category.md) | `GET /api/v1/measure-categories/{measure-category-code}/measures` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reported Measure Categories](actions/list-reported-measure-categories.md) | `GET /api/v1/reported-measure-categories` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reported Measures](actions/list-reported-measures.md) | `GET /api/v1/reported-measures` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reported Measures For Category](actions/list-reported-measures-for-category.md) | `GET /api/v1/reported-measure-categories/{reported-measure-category-code}/reported-measures` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reporting Unit Types](actions/list-reporting-unit-types.md) | `GET /api/v1/reporting-unit-types` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reporting Units](actions/list-reporting-units.md) | `GET /api/v1/reporting-units` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
| [List Reporting Units Available For Measure](actions/list-reporting-units-available-for-measure.md) | `GET /api/v1/measures/{measure-code}/reporting-units-available` | [docs](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json) |
