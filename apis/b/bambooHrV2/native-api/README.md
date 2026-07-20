# BambooHR: Native API Reference

A consolidated summary of BambooHR's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://documentation.bamboohr.com/docs
- **API base URL:** `https://mindcloud.bamboohr.com/api`

## Authentication

### OAuth2

Connect BambooHR with OAuth2 for the MindCloud tenant using the Linear-approved BambooHR scope set, excluding stale company:info because BambooHR does not expose it as a valid OAuth scope.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://mindcloud.bamboohr.com/authorize.php to approve access.
2. Exchange the returned authorization code with a POST request to https://mindcloud.bamboohr.com/token.php.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid offline_access email employee time_off employee:name employee:job payroll benefit`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://mindcloud.bamboohr.com/token.php.

[Official authentication documentation](https://documentation.bamboohr.com/docs/getting-started)

### Basic

Use BambooHR API key authentication for BambooHR endpoints that do not support OAuth2. Enter the BambooHR API key; MindCloud will send it as the Basic username and auto-fill the placeholder password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://documentation.bamboohr.com/docs/api-key-permissions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page[limit]` in the query string to set the page size (default 50). Use `page[after]` in the query string as the pagination cursor.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Time Off Request](actions/add-time-off-request.md) | `PUT /v1/employees/:employeeId/time_off/request` | [docs](https://documentation.bamboohr.com/reference/time-off-add-a-time-off-request) |
| [Change Request Status](actions/change-request-status.md) | `PUT /v1/time_off/requests/:requestId/status` | [docs](https://documentation.bamboohr.com/reference/time-off-change-a-request-status) |
| [Create Employee](actions/create-employee.md) | `POST /v1/employees` | [docs](https://documentation.bamboohr.com/reference/add-employee-2) |
| [Get Benefit Coverages](actions/get-benefit-coverages.md) | `GET /v1/benefitcoverages` | [docs](https://documentation.bamboohr.com/reference/get-benefit-coverages-2) |
| [Get Benefit Deduction Types](actions/get-benefit-deduction-types.md) | `GET /v1/benefits/settings/deduction_types/all` | [docs](https://documentation.bamboohr.com/reference/get-benefit-deduction-types-2) |
| [Get Changed Employees](actions/get-changed-employees.md) | `GET /v1/employees/changed/[:type]` | [docs](https://documentation.bamboohr.com/reference/changed-employee-ids) |
| [Get Company Benefits](actions/get-company-benefits.md) | `GET /v1/benefit/company_benefit` | [docs](https://documentation.bamboohr.com/reference/get-company-benefits-1) |
| [Get Company Information](actions/get-company-information.md) | `GET /v1/company_information` | [docs](https://documentation.bamboohr.com/reference/get-company-information-1) |
| [Get Datasets](actions/get-datasets.md) | `GET /v1/datasets` | [docs](https://documentation.bamboohr.com/reference/get-datasets) |
| [Get Employee](actions/get-employee.md) | `GET /v1/employees/:id` | [docs](https://documentation.bamboohr.com/reference/get-employee-1) |
| [Get Employee Benefits](actions/get-employee-benefits.md) | `GET /v1/benefit/employee_benefit` | [docs](https://documentation.bamboohr.com/reference/get-employee-benefit-1) |
| [Get Employee Dependent](actions/get-employee-dependent.md) | `GET /v1/employeedependents/:id` | [docs](https://documentation.bamboohr.com/reference/get-employee-dependent-2) |
| [Get Employee Dependents](actions/get-employee-dependents.md) | `GET /v1/employeedependents` | [docs](https://documentation.bamboohr.com/reference/get-employee-dependents-2) |
| [Get Employee Directory](actions/get-employee-directory.md) | `GET /v1/employees/directory` | [docs](https://documentation.bamboohr.com/reference/get-employees-directory) |
| [Get Fields](actions/get-fields.md) | `GET /v1/meta/fields` | [docs](https://documentation.bamboohr.com/reference/metadata-get-a-list-of-fields-1) |
| [Get Fields from Dataset](actions/get-fields-from-dataset.md) | `GET /v1/datasets/:datasetName/fields` | [docs](https://documentation.bamboohr.com/reference/get-fields-from-dataset-2) |
| [Get List Field Details](actions/get-list-field-details.md) | `GET /v1/meta/lists` | [docs](https://documentation.bamboohr.com/reference/metadata-get-details-for-list-fields) |
| [Get Member Benefit Events](actions/get-member-benefit-events.md) | `GET /v1/benefit/member_benefit` | [docs](https://documentation.bamboohr.com/reference/get-member-benefit-2) |
| [Get Member Benefits](actions/get-member-benefits.md) | `GET /v1/benefits/member-benefits` | [docs](https://documentation.bamboohr.com/reference/get-member-benefits) |
| [Get Report by ID](actions/get-report-by-id.md) | `GET /v1/custom-reports/:reportId` | [docs](https://documentation.bamboohr.com/reference/getbyreportid-2) |
| [Get Reports](actions/get-reports.md) | `GET /v1/custom-reports` | [docs](https://documentation.bamboohr.com/reference/custom-reports-1) |
| [Get Tabular Fields](actions/get-tabular-fields.md) | `GET /v1/meta/tables` | [docs](https://documentation.bamboohr.com/reference/metadata-get-a-list-of-tabular-fields) |
| [Get Time Off Balance](actions/get-time-off-balance.md) | `GET /v1/employees/:employeeId/time_off/calculator` | [docs](https://documentation.bamboohr.com/reference/time-off-get-time-off-balance) |
| [Get Time Off Policies](actions/get-time-off-policies.md) | `GET /v1/meta/time_off/policies` | [docs](https://documentation.bamboohr.com/reference/get-time-off-policies-1) |
| [Get Time Off Policies for Employee](actions/get-time-off-policies-for-employee.md) | `GET /v1/employees/:employeeId/time_off/policies` | [docs](https://documentation.bamboohr.com/reference/time-off-list-time-off-policies-for-employee-1) |
| [Get Time Off Requests](actions/get-time-off-requests.md) | `GET /v1/time_off/requests` | [docs](https://documentation.bamboohr.com/reference/time-off-get-time-off-requests) |
| [Get Time Off Types](actions/get-time-off-types.md) | `GET /v1/meta/time_off/types` | [docs](https://documentation.bamboohr.com/reference/get-time-off-types-1) |
| [Get Users](actions/get-users.md) | `GET /v1/meta/users` | [docs](https://documentation.bamboohr.com/reference/get-list-of-users-1) |
| [Get Who's Out](actions/get-whos-out.md) | `GET /v1/time_off/whos_out` | [docs](https://documentation.bamboohr.com/reference/get-a-list-of-who-is-out-1) |
| [List Employees](actions/list-employees.md) | `GET /v1/employees` | [docs](https://documentation.bamboohr.com/reference/get-employees-list) |
| [Update Employee](actions/update-employee.md) | `POST /v1/employees/:employeeId` | [docs](https://documentation.bamboohr.com/reference/update-employee-1) |
