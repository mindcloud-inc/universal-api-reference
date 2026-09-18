# Paycom: Native API Reference

A consolidated summary of Paycom's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://drive.google.com/drive/folders/1Ug5PtxNyl2okfXJvsiZqWyqhZwS3XkBY?usp=sharing
- **API base URL:** `https://api.paycomonline.net/v4/rest/index.php/`

## Authentication

### Custom

### Credentials

- **SID:** `sid` · optional
- **Token:** `token` · optional

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `pagesize` in the query string to set the page size (default 500; accepted range 1–500). Use `requestid` in the query string as the pagination cursor; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Clocked In/Out Status](actions/get-clocked-in-out-status.md) | `GET api/v1/clockedinoutstatus/:employeeCode` |  |
| [Get Employee](actions/get-employee.md) | `GET api/v1/employee/:eecode/:sensitive` |  |
| [Get Employee Custom Fields](actions/get-employee-custom-fields.md) | `GET api/v1/employee/:eecode/customfield` |  |
| [Get Employee Effective Rate](actions/get-employee-effective-rate.md) | `GET api/v1/employee/:eecode/effectiveratesbyallocation` |  |
| [Get Employee New Hire](actions/get-employee-new-hire.md) | `GET api/v1/employeenewhire` |  |
| [Get Employee Rate](actions/get-employee-rate.md) | `GET api/v1/employee/:eecode/ratesbyallocation` |  |
| [Get Employee Sensitive](actions/get-employee-sensitive.md) | `GET api/v1/employee/:eecode/sensitive` |  |
| [Get Punch Audit](actions/get-punch-audit.md) | `GET api/v1/employee/:eecode/punchaudit` |  |
| [Get Punch History](actions/get-punch-history.md) | `GET api/v1/employee/:employeeCode/punchhistory` |  |
| [List Employee Changed](actions/list-employee.md) | `GET api/v1/employee/:eecode/change` |  |
| [List Employee Changes](actions/list-employee-changes.md) | `GET api/v1/employeeids/employeechanges` |  |
| [List Employees](actions/list-employees.md) | `GET api/v1/employeedirectory` |  |
| [List Employees Active](actions/list-employees-active.md) | `GET api/v1/employeeid` |  |
| [List Employee ids](actions/list-employees-ids.md) | `GET api/v1/employeeid` |  |
| [List Employees Sensitive Changes](actions/list-employees-sensitive-changes.md) | `GET api/v1/employee/:eecode/sensitivechange` |  |
| [List Locations](actions/list-locations.md) | `GET api/v1/cl/locations` | [docs](https://drive.google.com/drive/folders/1Ug5PtxNyl2okfXJvsiZqWyqhZwS3XkBY?usp=sharing) |
