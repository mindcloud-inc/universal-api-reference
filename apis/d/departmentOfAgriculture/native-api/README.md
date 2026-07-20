# Department of Agriculture: Native API Reference

A consolidated summary of Department of Agriculture's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.ers.usda.gov/developer/data-apis/arms-data-api
- **API base URL:** `https://api.ers.usda.gov/data`

## Authentication

### API Key

Use a data.gov API key for USDA ERS ARMS API requests. MindCloud maps the stored key to the shared `api_key` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.data.gov/signup/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get ARMS Survey Data](actions/get-arms-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get ARMS Survey Data by Report](actions/get-arms-survey-data-by-report.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Farm Business Balance Sheet Survey Data](actions/get-farm-business-balance-sheet-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Farm Business Debt Repayment Capacity Survey Data](actions/get-farm-business-debt-repayment-capacity-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Farm Business Financial Ratios Survey Data](actions/get-farm-business-financial-ratios-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Farm Business Income Statement Survey Data](actions/get-farm-business-income-statement-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Government Payments Survey Data](actions/get-government-payments-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Operator Household Balance Sheet Survey Data](actions/get-operator-household-balance-sheet-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Operator Household Income Survey Data](actions/get-operator-household-income-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Get Structural Characteristics Survey Data](actions/get-structural-characteristics-survey-data.md) | `GET /arms/surveydata` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS Categories](actions/list-arms-categories.md) | `GET /arms/category` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS Farm Types](actions/list-arms-farm-types.md) | `GET /arms/farmtype` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS Reports](actions/list-arms-reports.md) | `GET /arms/report` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS States](actions/list-arms-states.md) | `GET /arms/state` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS Variables](actions/list-arms-variables.md) | `GET /arms/variable` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [List ARMS Years](actions/list-arms-years.md) | `GET /arms/year` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Search ARMS Categories](actions/search-arms-categories.md) | `GET /arms/category` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Search ARMS Farm Types](actions/search-arms-farm-types.md) | `GET /arms/farmtype` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Search ARMS Reports](actions/search-arms-reports.md) | `GET /arms/report` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
| [Search ARMS Variables](actions/search-arms-variables.md) | `GET /arms/variable` | [docs](https://www.ers.usda.gov/developer/data-apis/arms-data-api) |
