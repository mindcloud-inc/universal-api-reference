# Environmental Protection Agency: Native API Reference

A consolidated summary of Environmental Protection Agency's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://aqs.epa.gov/aqsweb/documents/data_api.html
- **OpenAPI specification:** https://aqs.epa.gov/aqsweb/documents/aqs_api_specification.json
- **API base URL:** `https://aqs.epa.gov/data/api`

## Authentication

### API Key

EPA AQS requests require the registered email address and matching API key as query parameters.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required · Email address registered with EPA AQS. EPA requires this to match the API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://aqs.epa.gov/aqsweb/documents/data_api.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `Body`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 5000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Availability](actions/check-api-availability.md) | `GET /metaData/isAvailable` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#metadata) |
| [Get Annual Data By Box](actions/get-annual-data-by-box.md) | `GET /annualData/byBox` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#annual-summary) |
| [Get Annual Data By CBSA](actions/get-annual-data-by-cbsa.md) | `GET /annualData/byCBSA` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#annual-summary) |
| [Get Annual Data By County](actions/get-annual-data-by-county.md) | `GET /annualData/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#annual-summary) |
| [Get Annual Data By Site](actions/get-annual-data-by-site.md) | `GET /annualData/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#annual-summary) |
| [Get Annual Data By State](actions/get-annual-data-by-state.md) | `GET /annualData/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#annual-summary) |
| [Get Daily Data By Box](actions/get-daily-data-by-box.md) | `GET /dailyData/byBox` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data) |
| [Get Daily Data By CBSA](actions/get-daily-data-by-cbsa.md) | `GET /dailyData/byCBSA` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data) |
| [Get Daily Data By County](actions/get-daily-data-by-county.md) | `GET /dailyData/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data) |
| [Get Daily Data By Site](actions/get-daily-data-by-site.md) | `GET /dailyData/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data) |
| [Get Daily Data By State](actions/get-daily-data-by-state.md) | `GET /dailyData/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily-summary-data) |
| [Get Monitors By Box](actions/get-monitors-by-box.md) | `GET /monitors/byBox` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors) |
| [Get Monitors By CBSA](actions/get-monitors-by-cbsa.md) | `GET /monitors/byCBSA` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors) |
| [Get Monitors By County](actions/get-monitors-by-county.md) | `GET /monitors/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors) |
| [Get Monitors By Site](actions/get-monitors-by-site.md) | `GET /monitors/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors) |
| [Get Monitors By State](actions/get-monitors-by-state.md) | `GET /monitors/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#monitors) |
| [Get QA Annual Performance Evaluations By County](actions/get-qa-annual-performance-evaluations-by-county.md) | `GET /qaAnnualPerformanceEvaluations/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#qa-annual-performance-evaluations) |
| [Get QA Annual Performance Evaluations By Site](actions/get-qa-annual-performance-evaluations-by-site.md) | `GET /qaAnnualPerformanceEvaluations/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#qa-annual-performance-evaluations) |
| [Get QA Annual Performance Evaluations By State](actions/get-qa-annual-performance-evaluations-by-state.md) | `GET /qaAnnualPerformanceEvaluations/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#qa-annual-performance-evaluations) |
| [Get Quarterly Data By Box](actions/get-quarterly-data-by-box.md) | `GET /quarterlyData/byBox` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#quarterly-summary) |
| [Get Quarterly Data By CBSA](actions/get-quarterly-data-by-cbsa.md) | `GET /quarterlyData/byCBSA` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#quarterly-summary) |
| [Get Quarterly Data By County](actions/get-quarterly-data-by-county.md) | `GET /quarterlyData/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#quarterly-summary) |
| [Get Quarterly Data By Site](actions/get-quarterly-data-by-site.md) | `GET /quarterlyData/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#quarterly-summary) |
| [Get Quarterly Data By State](actions/get-quarterly-data-by-state.md) | `GET /quarterlyData/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#quarterly-summary) |
| [Get Sample Data By Box](actions/get-sample-data-by-box.md) | `GET /sampleData/byBox` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data) |
| [Get Sample Data By CBSA](actions/get-sample-data-by-cbsa.md) | `GET /sampleData/byCBSA` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data) |
| [Get Sample Data By County](actions/get-sample-data-by-county.md) | `GET /sampleData/byCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data) |
| [Get Sample Data By Site](actions/get-sample-data-by-site.md) | `GET /sampleData/bySite` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data) |
| [Get Sample Data By State](actions/get-sample-data-by-state.md) | `GET /sampleData/byState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data) |
| [List CBSAs](actions/list-cbsas.md) | `GET /list/cbsas` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List Counties By State](actions/list-counties-by-state.md) | `GET /list/countiesByState` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List Fields By Service](actions/list-fields-by-service.md) | `GET /metaData/fieldsByService` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#metadata) |
| [List Known Issues](actions/list-known-issues.md) | `GET /metaData/issues` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#metadata) |
| [List Monitoring Agencies](actions/list-monitoring-agencies.md) | `GET /list/mas` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List Parameter Classes](actions/list-parameter-classes.md) | `GET /list/classes` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List Parameters By Class](actions/list-parameters-by-class.md) | `GET /list/parametersByClass` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List PQAOs](actions/list-pqaos.md) | `GET /list/pqaos` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List Revision History](actions/list-revision-history.md) | `GET /metaData/revisionHistory` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#metadata) |
| [List Sites By County](actions/list-sites-by-county.md) | `GET /list/sitesByCounty` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
| [List States](actions/list-states.md) | `GET /list/states` | [docs](https://aqs.epa.gov/aqsweb/documents/data_api.html#lists) |
