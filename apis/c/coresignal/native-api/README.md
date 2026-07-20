# Coresignal: Native API Reference

A consolidated summary of Coresignal's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://docs.coresignal.com
- **API base URL:** `https://api.coresignal.com/cdapi/v2`

## Authentication

### API Key

Coresignal requires an apikey request header on every API call.

### Credentials

- **API Key:** `apiKey` · required · Your Coresignal API key from the self-service dashboard.

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://docs.coresignal.com/api-introduction/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Collect Base Companies By DSL](actions/bulk-collect-base-companies-by-dsl.md) | `POST /data_requests/company_base/es_dsl` | [docs](https://docs.coresignal.com/company-api/base-company-api/endpoints/bulk-collect-companies) |
| [Bulk Collect Base Companies By Filters](actions/bulk-collect-base-companies-by-filters.md) | `POST /data_requests/company_base/filter` | [docs](https://docs.coresignal.com/company-api/base-company-api/endpoints/bulk-collect-companies) |
| [Bulk Collect Base Employees By DSL](actions/bulk-collect-base-employees-by-dsl.md) | `POST /data_requests/employee_base/es_dsl` | [docs](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/bulk-collect-profiles) |
| [Bulk Collect Base Employees By Filters](actions/bulk-collect-base-employees-by-filters.md) | `POST /data_requests/employee_base/filter` | [docs](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/bulk-collect-profiles) |
| [Bulk Collect Base Employees By Shorthand Names](actions/bulk-collect-base-employees-by-shorthand-names.md) | `POST /data_requests/employee_base/shorthand_names` | [docs](https://docs.coresignal.com/employee-api/base-employee-api) |
| [Bulk Collect Base Employees By URLs](actions/bulk-collect-base-employees-by-urls.md) | `POST /data_requests/employee_base/urls` | [docs](https://docs.coresignal.com/employee-api/base-employee-api) |
| [Bulk Collect Base Jobs By Filters](actions/bulk-collect-base-jobs-by-filters.md) | `POST /data_requests/job_base/filter` | [docs](https://docs.coresignal.com/job-api/base-job-api/endpoints/bulk-collect-jobs) |
| [Bulk Collect Clean Companies By DSL](actions/bulk-collect-clean-companies-by-dsl.md) | `POST /data_requests/company_clean/es_dsl` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Bulk Collect Clean Companies By IDs](actions/bulk-collect-clean-companies-by-ids.md) | `POST /data_requests/company_clean/ids` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Bulk Collect Clean Companies By Shorthand Names](actions/bulk-collect-clean-companies-by-shorthand-names.md) | `POST /data_requests/company_clean/shorthand_names` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Bulk Collect Clean Companies By URLs](actions/bulk-collect-clean-companies-by-urls.md) | `POST /data_requests/company_clean/urls` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Bulk Collect Multi-source Companies By DSL](actions/bulk-collect-multi-source-companies-by-dsl.md) | `POST /data_requests/company_multi_source/es_dsl` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api) |
| [Bulk Collect Multi-source Companies By IDs](actions/bulk-collect-multi-source-companies-by-ids.md) | `POST /data_requests/company_multi_source/ids` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api) |
| [Bulk Collect Multi-source Employees By IDs](actions/bulk-collect-multi-source-employees-by-ids.md) | `POST /data_requests/employee_multi_source/ids` | [docs](https://docs.coresignal.com/employee-api/multi-source-employee-api) |
| [Bulk Collect Multi-source Jobs By DSL](actions/bulk-collect-multi-source-jobs-by-dsl.md) | `POST /data_requests/job_multi_source/es_dsl` | [docs](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/bulk-collect) |
| [Bulk Collect Multi-source Jobs By IDs](actions/bulk-collect-multi-source-jobs-by-ids.md) | `POST /data_requests/job_multi_source/ids` | [docs](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/bulk-collect) |
| [Collect Base Company By ID](actions/collect-base-company-by-id.md) | `GET /company_base/collect/:companyId` | [docs](https://docs.coresignal.com/company-api/base-company-api/endpoints/collect-company) |
| [Collect Base Employee By ID](actions/collect-base-employee-by-id.md) | `GET /employee_base/collect/:employeeId` | [docs](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/collect-profile) |
| [Collect Base Employee By Identifier](actions/collect-base-employee-by-identifier.md) | `GET /employee_base/collect/:employeeIdentifier` | [docs](https://docs.coresignal.com/employee-api/base-employee-api) |
| [Collect Base Job By ID](actions/collect-base-job-by-id.md) | `GET /job_base/collect/:jobId` | [docs](https://docs.coresignal.com/job-api/base-job-api/endpoints/collect-job) |
| [Collect Clean Company By ID](actions/collect-clean-company-by-id.md) | `GET /company_clean/collect/:companyId` | [docs](https://docs.coresignal.com/company-api/clean-company-api/endpoints/collect-company) |
| [Collect Clean Company By Identifier](actions/collect-clean-company-by-identifier.md) | `GET /company_clean/collect/:companyIdentifier` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Collect Clean Employee By ID](actions/collect-clean-employee-by-id.md) | `GET /employee_clean/collect/:employeeId` | [docs](https://docs.coresignal.com/employee-api/clean-employee-api/endpoints/collect-profile) |
| [Collect Clean Employee By Identifier](actions/collect-clean-employee-by-identifier.md) | `GET /employee_clean/collect/:employeeIdentifier` | [docs](https://docs.coresignal.com/employee-api/clean-employee-api) |
| [Collect Multi-source Company By ID](actions/collect-multi-source-company-by-id.md) | `GET /company_multi_source/collect/:companyId` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api/endpoints/collect-company) |
| [Collect Multi-source Company By Identifier](actions/collect-multi-source-company-by-identifier.md) | `GET /company_multi_source/collect/:companyIdentifier` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api) |
| [Collect Multi-source Employee By ID](actions/collect-multi-source-employee-by-id.md) | `GET /employee_multi_source/collect/:employeeId` | [docs](https://docs.coresignal.com/employee-api/multi-source-employee-api/endpoints/collect-profile) |
| [Collect Multi-source Employee By Identifier](actions/collect-multi-source-employee-by-identifier.md) | `GET /employee_multi_source/collect/:employeeIdentifier` | [docs](https://docs.coresignal.com/employee-api/multi-source-employee-api) |
| [Collect Multi-source Job By ID](actions/collect-multi-source-job-by-id.md) | `GET /job_multi_source/collect/:jobId` | [docs](https://docs.coresignal.com/job-api/multi-source-job-api/endpoints/collect-job) |
| [Enrich Clean Company](actions/enrich-clean-company.md) | `GET /company_clean/enrich` | [docs](https://docs.coresignal.com/company-api/clean-company-api) |
| [Enrich Multi-source Company](actions/enrich-multi-source-company.md) | `GET /company_multi_source/enrich` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api/enrich) |
| [List Data Request Files](actions/list-data-request-files.md) | `GET /data_requests/:dataRequestId/files` | [docs](https://docs.coresignal.com/api-introduction/download-center-and-bulk-data-requests) |
| [Preview Base Companies By DSL](actions/preview-base-companies-by-dsl.md) | `POST /company_base/search/es_dsl/preview` | [docs](https://docs.coresignal.com/company-api/base-company-api/endpoints/preview-companies) |
| [Preview Base Employees By DSL](actions/preview-base-employees-by-dsl.md) | `POST /employee_base/search/es_dsl/preview` | [docs](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/preview-profiles) |
| [Preview Base Jobs By DSL](actions/preview-base-jobs-by-dsl.md) | `POST /job_base/search/es_dsl/preview` | [docs](https://docs.coresignal.com/job-api/base-job-api/endpoints/preview-jobs) |
| [Preview Clean Companies By DSL](actions/preview-clean-companies-by-dsl.md) | `POST /company_clean/search/es_dsl/preview` | [docs](https://docs.coresignal.com/company-api/clean-company-api/endpoints/preview-companies) |
| [Preview Clean Employees By DSL](actions/preview-clean-employees-by-dsl.md) | `POST /employee_clean/search/es_dsl/preview` | [docs](https://docs.coresignal.com/employee-api/clean-employee-api/endpoints/preview-profiles) |
| [Preview Multi-source Companies By DSL](actions/preview-multi-source-companies-by-dsl.md) | `POST /company_multi_source/search/es_dsl/preview` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api/endpoints/preview-companies) |
| [Preview Multi-source Employees By DSL](actions/preview-multi-source-employees-by-dsl.md) | `POST /employee_multi_source/search/es_dsl/preview` | [docs](https://docs.coresignal.com/employee-api/multi-source-employee-api/endpoints/preview-profiles) |
| [Preview Multi-source Jobs By DSL](actions/preview-multi-source-jobs-by-dsl.md) | `POST /job_multi_source/search/es_dsl/preview` | [docs](https://docs.coresignal.com/job-api/multi-source-job-api/endpoints/preview-jobs) |
| [Search Base Companies By DSL](actions/search-base-companies-by-dsl.md) | `POST /company_base/search/es_dsl` | [docs](https://docs.coresignal.com/api/company-api-esdsl-endpoint) |
| [Search Base Employees By DSL](actions/search-base-employees-by-dsl.md) | `POST /employee_base/search/es_dsl` | [docs](https://docs.coresignal.com/api/base-employee-api-esdsl) |
| [Search Base Jobs By DSL](actions/search-base-jobs-by-dsl.md) | `POST /job_base/search/es_dsl` | [docs](https://docs.coresignal.com/jobs-api/base-jobs-api/endpoints/elasticsearch-dsl) |
| [Search Clean Companies By DSL](actions/search-clean-companies-by-dsl.md) | `POST /company_clean/search/es_dsl` | [docs](https://docs.coresignal.com/api/clean-company-api-esdsl-endpoint) |
| [Search Clean Employees By DSL](actions/search-clean-employees-by-dsl.md) | `POST /employee_clean/search/es_dsl` | [docs](https://docs.coresignal.com/api/clean-employee-api-esdsl-endpoint) |
| [Search Multi-source Companies By DSL](actions/search-multi-source-companies-by-dsl.md) | `POST /company_multi_source/search/es_dsl` | [docs](https://docs.coresignal.com/company-api/multi-source-company-api/elasticsearch-dsl) |
| [Search Multi-source Employees By DSL](actions/search-multi-source-employees-by-dsl.md) | `POST /employee_multi_source/search/es_dsl` | [docs](https://docs.coresignal.com/employee-api/multi-source-employee-api/elasticsearch-dsl) |
| [Search Multi-source Jobs By DSL](actions/search-multi-source-jobs-by-dsl.md) | `POST /job_multi_source/search/es_dsl` | [docs](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/elasticsearch-dsl) |
