# 7shifts: Native API Reference

A consolidated summary of 7shifts's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.7shifts.com/docs/getting-started
- **API base URL:** `https://api.7shifts.com`

## Authentication

### Access Token

Connect with a 7shifts access token and company GUID.

### Credentials

- **Access Token:** `accessToken` · required · 7shifts access token used as a bearer token in the Authorization header.
- **Company GUID:** `companyGuid` · required · 7shifts company GUID sent in the x-company-guid header.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
x-company-guid: <companyGuid>
```

[Official authentication documentation](https://developers.7shifts.com/docs/oauth-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `x-api-version` | `2025-03-01` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `meta.cursor.next`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gte`, `lte`.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | `POST /v2/company/{company_id}/departments` | [docs](https://developers.7shifts.com/reference/createdepartment) |
| [Create Employment Record](actions/create-employment-record.md) | `POST /v2/company/{company_id}/employment_records` | [docs](https://developers.7shifts.com/reference/createemploymentrecord) |
| [Create Location](actions/create-location.md) | `POST /v2/company/{company_id}/locations` | [docs](https://developers.7shifts.com/reference/createlocation) |
| [Create Role](actions/create-role.md) | `POST /v2/company/{company_id}/roles` | [docs](https://developers.7shifts.com/reference/createrole) |
| [Create Role Assignment](actions/create-role-assignment.md) | `POST /v2/company/{company_id}/users/{user_id}/role_assignments` | [docs](https://developers.7shifts.com/reference/createroleassignment) |
| [Create Shift](actions/create-shift.md) | `POST /v2/company/{company_id}/shifts` | [docs](https://developers.7shifts.com/reference/postshift) |
| [Create Time Punch](actions/create-time-punch.md) | `POST /v2/company/{company_id}/time_punches` | [docs](https://developers.7shifts.com/reference/posttimepunch) |
| [Create User](actions/create-user.md) | `POST /v2/company/{company_id}/users` | [docs](https://developers.7shifts.com/reference/postuser) |
| [Create User Wage](actions/create-user-wage.md) | `POST /v2/company/{company_id}/users/{user_id}/wages` | [docs](https://developers.7shifts.com/reference/createuserwages) |
| [Deactivate User](actions/deactivate-user.md) | `DELETE /v2/company/{company_id}/users/{identifier}` | [docs](https://developers.7shifts.com/reference/deactivateuser) |
| [Delete Shift](actions/delete-shift.md) | `DELETE /v2/company/{company_id}/shifts/{shift_id}` | [docs](https://developers.7shifts.com/reference/deleteshift) |
| [Get User Contacts](actions/get-user-contacts.md) | `GET /v2/company/{company_id}/contacts` | [docs](https://developers.7shifts.com/reference/listcontacts) |
| [List Assignments](actions/list-assignments.md) | `GET /v2/company/{company_id}/users/{user_id}/assignments` | [docs](https://developers.7shifts.com/reference/getassignments) |
| [List Companies](actions/list-companies.md) | `GET /v2/companies` | [docs](https://developers.7shifts.com/reference/listcompanies) |
| [List Departments](actions/list-departments.md) | `GET /v2/company/{company_id}/departments` | [docs](https://developers.7shifts.com/reference/listdepartments) |
| [List Employment Records](actions/list-employment-records.md) | `GET /v2/company/{company_id}/employment_records` | [docs](https://developers.7shifts.com/reference/listemploymentrecord) |
| [List Locations](actions/list-locations.md) | `GET /v2/company/{company_id}/locations` | [docs](https://developers.7shifts.com/reference/getlocationlistbycompany) |
| [List Role Assignments](actions/list-role-assignments.md) | `GET /v2/company/{company_id}/users/{user_id}/role_assignments` | [docs](https://developers.7shifts.com/reference/getroleassignments) |
| [List Roles](actions/list-roles.md) | `GET /v2/company/{company_id}/roles` | [docs](https://developers.7shifts.com/reference/listroles) |
| [List Shifts](actions/list-shifts.md) | `GET /v2/company/{company_id}/shifts` | [docs](https://developers.7shifts.com/reference/listshift) |
| [List Time Punches](actions/list-time-punches.md) | `GET /v2/company/{company_id}/time_punches` | [docs](https://developers.7shifts.com/reference/gettimepunches) |
| [List User Wages](actions/list-user-wages.md) | `GET /v2/company/{company_id}/users/{user_id}/wages` | [docs](https://developers.7shifts.com/reference/getuserwages) |
| [List Users](actions/list-users.md) | `GET /v2/company/{company_id}/users` | [docs](https://developers.7shifts.com/reference/listuserslist) |
| [List Users Authorized Locations](actions/list-users-authorized-locations.md) | `GET /v2/company/{company_id}/users/{user_id}/authorized_locations` | [docs](https://developers.7shifts.com/reference/listusersauthorizedlocations) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /v2/companies/{id}` | [docs](https://developers.7shifts.com/reference/viewcompany) |
| [Retrieve Department](actions/retrieve-department.md) | `GET /v2/company/{company_id}/departments/{department_id}` | [docs](https://developers.7shifts.com/reference/retrievedepartment) |
| [Retrieve Identity](actions/retrieve-identity.md) | `GET /v2/whoami` | [docs](https://developers.7shifts.com/reference/whoami) |
| [Retrieve Labor Settings](actions/retrieve-labor-settings.md) | `GET /v2/company/{company_id}/labor_settings` | [docs](https://developers.7shifts.com/reference/retrievecompanylaborsettings) |
| [Retrieve Location](actions/retrieve-location.md) | `GET /v2/company/{company_id}/locations/{location_id}` | [docs](https://developers.7shifts.com/reference/getlocationbyid) |
| [Retrieve Role](actions/retrieve-role.md) | `GET /v2/company/{company_id}/roles/{role_id}` | [docs](https://developers.7shifts.com/reference/retrieverole) |
| [Retrieve Shift](actions/retrieve-shift.md) | `GET /v2/company/{company_id}/shifts/{shift_id}` | [docs](https://developers.7shifts.com/reference/retrieveshift) |
| [Retrieve Time Punch](actions/retrieve-time-punch.md) | `GET /v2/company/{company_id}/time_punches/{time_punch_id}` | [docs](https://developers.7shifts.com/reference/gettimepunchbyid) |
| [Retrieve User](actions/retrieve-user.md) | `GET /v2/company/{company_id}/users/{identifier}` | [docs](https://developers.7shifts.com/reference/getuser) |
| [Retrieve User Contact](actions/retrieve-user-contact.md) | `GET /v2/company/{company_id}/contacts/{identifier}` | [docs](https://developers.7shifts.com/reference/getcontact) |
| [Update Department](actions/update-department.md) | `PUT /v2/company/{company_id}/departments/{department_id}` | [docs](https://developers.7shifts.com/reference/updatedepartment) |
| [Update Location](actions/update-location.md) | `PUT /v2/company/{company_id}/locations/{location_id}` | [docs](https://developers.7shifts.com/reference/updatelocation) |
| [Update Role](actions/update-role.md) | `PUT /v2/company/{company_id}/roles/{role_id}` | [docs](https://developers.7shifts.com/reference/updaterole) |
| [Update Shift](actions/update-shift.md) | `PUT /v2/company/{company_id}/shifts/{shift_id}` | [docs](https://developers.7shifts.com/reference/updateshift) |
| [Update Time Punch](actions/update-time-punch.md) | `PUT /v2/company/{company_id}/time_punches/{time_punch_id}` | [docs](https://developers.7shifts.com/reference/puttimepunch) |
| [Update User](actions/update-user.md) | `PUT /v2/company/{company_id}/users/{identifier}` | [docs](https://developers.7shifts.com/reference/putuser) |
