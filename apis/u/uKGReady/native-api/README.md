# UKG Ready: Native API Reference

A consolidated summary of UKG Ready's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://secure7.saashr.com/ta/docs/rest/public/
- **API base URL:** `https://{hostname}/ta/rest`

## Authentication

### Custom

### Credentials

- **User:** `user` · required
- **Password:** `password` · required
- **Api Key:** `apiKey` · required
- **Company:** `company` · required
- **Hostname:** `hostname` · required · The hostname from your UKG Ready login URL, without https:// or a path. The default preserves the server previously used by existing connections; change it if your company uses another server.

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

### OAuth2 (M2M)

Connect using your company's UKG Ready hostname and Machine to Machine OAuth application.

### Credentials

- **Company ID:** `companyId` · required · The API company ID provided by your UKG Ready administrator.
- **Hostname:** `hostname` · required · Copy the hostname from your UKG Ready login URL, without https:// or any path. Use your own company's server.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://{{credentials.hostname}}/ta/rest/v2/companies/{{credentials.companyId}}/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. A machine-to-machine flow is configured.

[Official authentication documentation](https://secure.saashr.com/ta/docs/rest/public/Client_id_and_secret.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Time Punches](actions/create-time-punches.md) | `POST /v2/companies/:cid/time-punches/collection` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /v2/companies/:cid/time-entries/:time_entry_id` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Account Assignments](actions/get-account-assignments.md) | `GET /v2/companies/:cid/position/assignments/:accountId` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Compensation per company](actions/get-compensation-per-company.md) | `GET /v2/companies/:cid/compensation/total` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee](actions/get-employee.md) | `GET /v2/companies/:cid/employees/:aid` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Attendance](actions/get-employee-attendance.md) | `GET /v2/companies/:cid/employees/:employeeId/attendance` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Badges](actions/get-employee-badges.md) | `GET /v2/companies/:cid/employees/:employeeId/badges` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Contact](actions/get-employee-contact.md) | `GET /v2/companies/:cid/employees/:employeeId/contacts` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Demographics](actions/get-employee-demographics.md) | `GET /v2/companies/:cid/employees/:employeeId/demographics` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Detail](actions/get-employee-detail.md) | `GET /v2/companies/:cid/employees/:employeeId` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Pay Info](actions/get-employee-pay-info.md) | `GET /v2/companies/:cid/employees/:employeeId/pay-info` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Employee Profiles](actions/get-employee-profiles.md) | `GET /v2/companies/:cid/employees/:employeeId/profiles` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Get Pay Types](actions/get-pay-types.md) | `GET /v1/employee/accrual-balances` | [docs](https://secure7.saashr.com/ta/docs/rest/public/) |
| [List Cost Centers](actions/list-cost-centers.md) | `GET /v2/companies/:cid/config/cost-centers` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [List Employee Time Entries](actions/list-employee-time-entries.md) | `GET /v2/companies/:cid/employees/:employeeId/time-entries` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [List Employees](actions/list-employees.md) | `GET /v2/companies/:resolvedCid/employees/` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [List Jobs](actions/list-jobs.md) | `GET /v2/companies/:cid/lookup/jobs` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [List Time Entries](actions/list-time-entries.md) | `GET /v2/companies/:cid/time-entries` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
| [Update Time Entries](actions/update-time-entries.md) | `PUT /v2/companies/:cid/time-entries/collection` | [docs](https://secure7.saashr.com/ta/docs/rest/public) |
