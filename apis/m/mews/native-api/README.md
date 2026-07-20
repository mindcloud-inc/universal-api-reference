# Mews: Native API Reference

A consolidated summary of Mews's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.mews.com/connector-api/
- **API base URL:** `{platformAddress}/api/connector/v1`

## Authentication

### Connector API Tokens

Use a Mews ClientToken, AccessToken, and Platform Address to authenticate Connector API requests.

### Credentials

- **Client Token:** `clientToken` · required · Token identifying the Mews client application.
- **Access Token:** `accessToken` · required · Access token identifying the connected Mews enterprise or property.
- **Platform Address:** `platformAddress` · required · Environment-specific Mews platform address, such as https://api.mews-demo.com or https://api.mews.com.

[Official authentication documentation](https://docs.mews.com/connector-api/guidelines/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `cursor`.

## Pagination

Use `Count` in the request body to set the page size (default 100; accepted range 1–1000). Use `Cursor` in the request body as the pagination cursor.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task](actions/add-task.md) | `POST /tasks/add` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/tasks.md#add-task) |
| [Get All Accounting Categories](actions/get-all-accounting-categories.md) | `POST /accountingCategories/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/accountingcategories.md) |
| [Get All Age Categories](actions/get-all-age-categories.md) | `POST /ageCategories/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/agecategories.md) |
| [Get All Business Segments](actions/get-all-business-segments.md) | `POST /businessSegments/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/businesssegments.md) |
| [Get All Cashiers](actions/get-all-cashiers.md) | `POST /cashiers/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/cashiers.md) |
| [Get All Companies](actions/get-all-companies.md) | `POST /companies/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/companies.md) |
| [Get All Counters](actions/get-all-counters.md) | `POST /counters/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/counters.md) |
| [Get All Currencies](actions/get-all-currencies.md) | `POST /currencies/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/currencies.md) |
| [Get All Departments](actions/get-all-departments.md) | `POST /departments/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/departments.md) |
| [Get All Exchange Rates](actions/get-all-exchange-rates.md) | `POST /exchangeRates/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/exchangerates.md) |
| [Get All Languages](actions/get-all-languages.md) | `POST /languages/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/languages.md) |
| [Get All Outlets](actions/get-all-outlets.md) | `POST /outlets/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/outlets.md) |
| [Get All Resource Categories](actions/get-all-resource-categories.md) | `POST /resourceCategories/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/resourcecategories.md#get-all-resource-categories) |
| [Get All Resource Features](actions/get-all-resource-features.md) | `POST /resourceFeatures/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/resourcefeatures.md#get-all-resource-features) |
| [Get All Resources](actions/get-all-resources.md) | `POST /resources/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/resources.md#get-all-resources) |
| [Get All Services](actions/get-all-services.md) | `POST /services/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/services.md) |
| [Get All Sources](actions/get-all-sources.md) | `POST /sources/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/sources.md#get-all-sources) |
| [Get All Tasks](actions/get-all-tasks.md) | `POST /tasks/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/tasks.md#get-all-tasks) |
| [Get All Tax Environments](actions/get-all-tax-environments.md) | `POST /taxEnvironments/getAll` | [docs](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/taxenvironments.md) |
| [Get Configuration](actions/get-configuration.md) | `POST /configuration/get` | [docs](https://docs.mews.com/connector-api/operations/configuration) |
