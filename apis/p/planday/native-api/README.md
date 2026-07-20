# Planday: Native API Reference

A consolidated summary of Planday's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://openapi.planday.com/
- **API base URL:** `https://openapi.planday.com`

## Authentication

### OAuth2

Connect Planday with OAuth2 for workforce and scheduling actions

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://id.planday.com/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://id.planday.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid offline_access department:read department:create department:update employee:read employee:create employee:update shiftposition:read shiftposition:create shiftposition:update shift:read shift:create shift:update shift:delete shifttype:read absence:read absence:create punchclockshift:read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://id.planday.com/connect/token.

[Official authentication documentation](https://developer.planday.com/gettingstarted/authorization-flow/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `offset` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Shift](actions/assign-shift.md) | `POST /scheduling/v1.0/shifts/:shiftId/employee` | [docs](https://openapi.planday.com/api/schedule/) |
| [Create Absence Request](actions/create-absence-request.md) | `POST /absence/v1.0/absencerequests` | [docs](https://openapi.planday.com/api/absence/) |
| [Create Department](actions/create-department.md) | `POST /hr/v1.0/departments` | [docs](https://openapi.planday.com/api/hr/) |
| [Create Employee](actions/create-employee.md) | `POST /hr/v1.0/employees` | [docs](https://openapi.planday.com/api/hr/) |
| [Create Position](actions/create-position.md) | `POST /scheduling/v1.0/positions` | [docs](https://openapi.planday.com/api/schedule/) |
| [Create Shift](actions/create-shift.md) | `POST /scheduling/v1.0/shifts` | [docs](https://openapi.planday.com/api/schedule/) |
| [Deactivate Employee](actions/deactivate-employee.md) | `PUT /hr/v1.0/employees/deactivate/:employeeId` | [docs](https://openapi.planday.com/api/hr/) |
| [Delete Shift](actions/delete-shift.md) | `DELETE /scheduling/v1.0/shifts/:shiftId` | [docs](https://openapi.planday.com/api/schedule/) |
| [Get Department](actions/get-department.md) | `GET /hr/v1.0/departments/:id` | [docs](https://openapi.planday.com/api/hr/) |
| [Get Employee](actions/get-employee.md) | `GET /hr/v1.0/employees/:employeeId` | [docs](https://openapi.planday.com/api/hr/) |
| [Get Portal Information](actions/get-portal-information.md) | `GET /portal/v1.0/info` | [docs](https://openapi.planday.com/api/portal/) |
| [Get Position](actions/get-position.md) | `GET /scheduling/v1.0/positions/:positionId` | [docs](https://openapi.planday.com/api/schedule/) |
| [Get Shift](actions/get-shift.md) | `GET /scheduling/v1.0/shifts/:shiftId` | [docs](https://openapi.planday.com/api/schedule/) |
| [List Absence Requests](actions/list-absence-requests.md) | `GET /absence/v1.0/absencerequests` | [docs](https://openapi.planday.com/api/absence/) |
| [List Absence Types](actions/list-absence-types.md) | `GET /absence/v1.0/absencetypes` | [docs](https://openapi.planday.com/api/absence/) |
| [List Deactivated Employees](actions/list-deactivated-employees.md) | `GET /hr/v1.0/employees/deactivated` | [docs](https://openapi.planday.com/api/hr/) |
| [List Department Employees](actions/list-department-employees.md) | `GET /hr/v1.0/departments/:id/employees` | [docs](https://openapi.planday.com/api/hr/) |
| [List Departments](actions/list-departments.md) | `GET /hr/v1.0/departments` | [docs](https://openapi.planday.com/api/hr/) |
| [List Employees](actions/list-employees.md) | `GET /hr/v1.0/employees` | [docs](https://openapi.planday.com/api/hr/) |
| [List Positions](actions/list-positions.md) | `GET /scheduling/v1.0/positions` | [docs](https://openapi.planday.com/api/schedule/) |
| [List Punch Clock Records](actions/list-punch-clock-records.md) | `GET /punchclock/v1.0/punchclockshifts` | [docs](https://openapi.planday.com/api/punchclock/) |
| [List Shift Statuses](actions/list-shift-statuses.md) | `GET /scheduling/v1.0/shifts/shiftstatus/all` | [docs](https://openapi.planday.com/api/schedule/) |
| [List Shift Types](actions/list-shift-types.md) | `GET /scheduling/v1.0/shifttypes` | [docs](https://openapi.planday.com/api/schedule/) |
| [List Shifts](actions/list-shifts.md) | `GET /scheduling/v1.0/shifts` | [docs](https://openapi.planday.com/api/schedule/) |
| [List Today's Employee Shifts](actions/list-todays-employee-shifts.md) | `GET /punchclock/v1.0/employeeshifts/today` | [docs](https://openapi.planday.com/api/punchclock/) |
| [Reactivate Employee](actions/reactivate-employee.md) | `PUT /hr/v1.0/employees/reactivate/:employeeId` | [docs](https://openapi.planday.com/api/hr/) |
| [Update Department](actions/update-department.md) | `PUT /hr/v1.0/departments/:id` | [docs](https://openapi.planday.com/api/hr/) |
| [Update Employee](actions/update-employee.md) | `PUT /hr/v1.0/employees/:employeeId` | [docs](https://openapi.planday.com/api/hr/) |
| [Update Position](actions/update-position.md) | `PUT /scheduling/v1.0/positions/:positionId` | [docs](https://openapi.planday.com/api/schedule/) |
| [Update Shift](actions/update-shift.md) | `PUT /scheduling/v1.0/shifts/:shiftId` | [docs](https://openapi.planday.com/api/schedule/) |
