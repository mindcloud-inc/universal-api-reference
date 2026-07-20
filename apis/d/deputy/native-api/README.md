# Deputy: Native API Reference

A consolidated summary of Deputy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.deputy.com/docs/getting-started-with-the-deputy-api
- **API base URL:** `https://{endpoint}.deputy.com`

## Authentication

### OAuth 2.0

### Credentials

- **Endpoint:** `endpoint` · required · Enter only your Deputy account subdomain.
Example: https://93929518050047.na.deputy.com -> 93929518050047.na

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://once.deputy.com/my/oauth/login to approve access.
2. Exchange the returned authorization code with a POST request to https://once.deputy.com/my/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `longlife_refresh_token`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://once.deputy.com/my/api/oauth/access_token.

[Official authentication documentation](https://developer.deputy.com/docs/using-oauth-20)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Shift](actions/add-shift.md) | `POST /api/v1/supervise/roster` | [docs](https://developer.deputy.com/docs/adding-a-shift) |
| [Create Employee](actions/create-employee.md) | `POST /api/management/v2/employees` | [docs](https://developer.deputy.com/docs/adding-an-employee) |
| [Create Leave Request](actions/create-leave-request.md) | `POST /api/v1/resource/Leave` | [docs](https://developer.deputy.com/docs/adding-a-leave-request-for-an-employee) |
| [Get Contact](actions/get-contact.md) | `GET /api/v1/resource/Contact/:id` | [docs](https://developer.deputy.com/docs/contact) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /api/v1/resource/CustomField/:id` | [docs](https://developer.deputy.com/docs/customfield) |
| [Get Employee](actions/get-employee.md) | `GET /api/v1/resource/Employee/:id` | [docs](https://developer.deputy.com/docs/employee) |
| [Get Leave Request](actions/get-leave-request.md) | `GET /api/v1/resource/Leave/:id` | [docs](https://developer.deputy.com/docs/leave) |
| [Get Timesheet Details](actions/get-timesheet-details.md) | `GET /api/v1/supervise/timesheet/:id/details` | [docs](https://developer.deputy.com/docs/timesheet-management-calls) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/resource/Contact` | [docs](https://developer.deputy.com/docs/contact) |
| [List Countries](actions/list-countries.md) | `POST /api/v1/resource/Country/QUERY` | [docs](https://developer.deputy.com/docs/retrieving-state-and-country-ids-for-use-with-the-deputy-api) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /api/v1/resource/CustomField` | [docs](https://developer.deputy.com/docs/customfield) |
| [List Employee Pay Conditions](actions/list-employee-pay-conditions.md) | `POST /api/v1/resource/EmployeeAgreement/QUERY` | [docs](https://developer.deputy.com/docs/retrieving-an-employees-pay-conditions) |
| [List Employees](actions/list-employees.md) | `GET /api/v1/resource/Employee` | [docs](https://developer.deputy.com/docs/employee) |
| [List Labor Model Rules](actions/list-labor-model-rules.md) | `GET /api/v2/labor-model/location/:locationId/rules` | [docs](https://developer.deputy.com/docs/retrieving-the-list-of-existing-labor-model-rules) |
| [List Leave Requests](actions/list-leave-requests.md) | `GET /api/v1/resource/Leave` | [docs](https://developer.deputy.com/docs/leave) |
| [List Sales Data](actions/list-sales-data.md) | `GET /api/v2/metrics/raw` | [docs](https://developer.deputy.com/docs/retrieving-sales-data-from-deputy) |
| [List Shifts](actions/list-shifts.md) | `POST /api/v1/resource/Roster/QUERY` | [docs](https://developer.deputy.com/docs/getting-shifts) |
| [List States](actions/list-states.md) | `POST /api/v1/resource/State/QUERY` | [docs](https://developer.deputy.com/docs/retrieving-state-and-country-ids-for-use-with-the-deputy-api) |
| [List Timesheet Pay Returns](actions/list-timesheet-pay-returns.md) | `POST /api/v1/resource/TimesheetPayReturn/QUERY` | [docs](https://developer.deputy.com/docs/retrieving-timesheets-from-deputy) |
| [List Timesheets](actions/list-timesheets.md) | `POST /api/v1/resource/Timesheet/QUERY` | [docs](https://developer.deputy.com/docs/retrieving-timesheets-from-deputy) |
| [Search Contacts](actions/search-contacts.md) | `POST /api/v1/resource/Contact/QUERY` | [docs](https://developer.deputy.com/docs/contact) |
| [Search Custom Fields](actions/search-custom-fields.md) | `POST /api/v1/resource/CustomField/QUERY` | [docs](https://developer.deputy.com/docs/customfield) |
| [Search Employees](actions/search-employees.md) | `POST /api/v1/resource/Employee/QUERY` | [docs](https://developer.deputy.com/docs/employee) |
| [Search Leave Requests](actions/search-leave-requests.md) | `POST /api/v1/resource/Leave/QUERY` | [docs](https://developer.deputy.com/docs/leave) |
