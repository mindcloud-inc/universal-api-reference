# Leave Dates: Native API Reference

A consolidated summary of Leave Dates's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://api.leavedates.com/documentation
- **OpenAPI specification:** https://api.leavedates.com/docs/api-docs.json
- **API base URL:** `https://api.leavedates.com`

## Authentication

### API Key

Authenticate Leave Dates requests with a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.leavedates.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

The page size is configurable (default 15; accepted range 15–15). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Department](actions/add-department.md) | `POST /departments` | [docs](https://api.leavedates.com/documentation#/Company/post_departments) |
| [Add Employment](actions/add-employment.md) | `POST /employments` | [docs](https://api.leavedates.com/documentation#/Employment/post_employments) |
| [Create Allowance Type](actions/create-allowance-type.md) | `POST /allowance-types` | [docs](https://api.leavedates.com/documentation#/Company/post_allowance-types) |
| [Create Leave Type](actions/create-leave-type.md) | `POST /leave-types` | [docs](https://api.leavedates.com/documentation#/Company/post_leave-types) |
| [Delete Allowance Type](actions/delete-allowance-type.md) | `DELETE /allowance-types/:id` | [docs](https://api.leavedates.com/documentation#/Company/delete_allowance-types__id_) |
| [Delete Department](actions/delete-department.md) | `DELETE /departments/:id` | [docs](https://api.leavedates.com/documentation#/Company/delete_departments__id_) |
| [Delete Employment](actions/delete-employment.md) | `DELETE /employments/:id` | [docs](https://api.leavedates.com/documentation#/Employment/delete_employments__id_) |
| [Delete Leave Type](actions/delete-leave-type.md) | `DELETE /leave-types/:id` | [docs](https://api.leavedates.com/documentation#/Company/delete_leave-types__id_) |
| [Get Allowance Type](actions/get-allowance-type.md) | `GET /allowance-types/:id` | [docs](https://api.leavedates.com/documentation#/Company/get_allowance-types__id_) |
| [Get Employment](actions/get-employment.md) | `GET /employments/:id` | [docs](https://api.leavedates.com/documentation#/Employment/get_employments__id_) |
| [Get Employment Report](actions/get-employment-report.md) | `GET /reports/employments` | [docs](https://api.leavedates.com/documentation#/Reporting/get_reports_employments) |
| [List Allowance Types](actions/list-allowance-types.md) | `GET /allowance-types` | [docs](https://api.leavedates.com/documentation#/Company/get_allowance-types) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://api.leavedates.com/documentation#/Company/get_companies) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://api.leavedates.com/documentation#/Company/get_countries) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://api.leavedates.com/documentation#/Company/get_departments) |
| [List Employments](actions/list-employments.md) | `GET /employments` | [docs](https://api.leavedates.com/documentation#/Employment/get_employments) |
| [List Leave Types](actions/list-leave-types.md) | `GET /leave-types` | [docs](https://api.leavedates.com/documentation#/Company/get_leave-types) |
| [Update Allowance Type](actions/update-allowance-type.md) | `PUT /allowance-types/:id` | [docs](https://api.leavedates.com/documentation#/Company/put_allowance-types__id_) |
| [Update Department](actions/update-department.md) | `PUT /departments/:id` | [docs](https://api.leavedates.com/documentation#/Company/put_departments__id_) |
| [Update Employment](actions/update-employment.md) | `PUT /employments/:id` | [docs](https://api.leavedates.com/documentation#/Employment/put_employments__id_) |
| [Update Leave Type](actions/update-leave-type.md) | `PUT /leave-types/:id` | [docs](https://api.leavedates.com/documentation#/Company/put_leave-types__id_) |
