# Paylocity: Native API Reference

A consolidated summary of Paylocity's API configuration and 5 documented operations.

- **API base URL:** `{connection}`

## Authentication

### NextGen API

Any API that is not a Weblink API

### Credentials

- **Client Id:** `clientId` · required
- **Client Secret:** `clientSecret` · required
- **Connection:** `connection` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–20). Use `nextToken` in the query string as the pagination cursor.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Employee Punch](actions/create-employee-punch.md) | `POST apihub/time/v2/companies/:companyId/punchImport` | [docs](https://developer.paylocity.com/integrations/reference/post_apihub_time_v2_companies_companyid_punchimport) |
| [Get Company Information](actions/get-company-information.md) | `GET apiHub/corehr/v1/companies/:companyId` | [docs](https://developer.paylocity.com/integrations/reference/get_apihub-corehr-v1-companies-companyid) |
| [Get Employee Punch Detail](actions/get-employee-punch-detail.md) | `GET apiHub/time/v1/companies/:companyId/employees/:employeeId/punchDetails` | [docs](https://developer.paylocity.com/integrations/reference/get_apihub_time_v1_companies_companyid_employees_employeeid_punchdetails) |
| [Get Employee Shifts](actions/get-employee-shifts.md) | `GET apiHub/scheduling/v1/companies/:companyId/employees/:employeeId/shifts` |  |
| [List Employees](actions/list-employees.md) | `GET coreHr/v1/companies/:companyId/employees` | [docs](https://developer.paylocity.com/integrations/reference/get_corehr-v1-companies-companyid-employees) |
