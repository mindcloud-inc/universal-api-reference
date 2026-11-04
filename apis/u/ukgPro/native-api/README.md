# UKG Pro: Native API Reference

A consolidated summary of UKG Pro's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.ukg.com/hcm/reference/welcome-to-the-pro-developer-hub
- **API base URL:** `https://{baseUrl}/`

## Authentication

### HTTP Basic authentication

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Base Url:** `baseUrl` · required
- **API Key:** `apiKey` · required · The API Key to connect to UKG Pro.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Employee Job History Details](actions/get-all-employee-job-history-details.md) | `GET personnel/v1/employee-job-history-details` |  |
| [Get All Org Levels](actions/get-all-org-levels.md) | `GET configuration/v1/org-levels` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details) |
| [Get Earnings History Base Elements](actions/get-earnings-history-base-elements.md) | `GET payroll/v1/earnings-history-base-elements` | [docs](https://developer.ukg.com/hcm/reference/earningshistory_getinsrate) |
| [Get Employee Changes](actions/get-employee-changes.md) | `GET personnel/v1/employee-changes/:employeeId` | [docs](https://developer.ukg.com/hcm/reference/employeechanges_get_all) |
| [Get Employee Demographic Details](actions/get-employee-demographic-details.md) | `GET personnel/v1/employee-demographic-details` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employee-demographic-details) |
| [Get Employee Employment Details](actions/get-employee-employment-details.md) | `GET personnel/v1/employee-employment-details` |  |
| [Get Employee Multiple Phone Numbers](actions/get-employee-multiple-phone-numbers.md) | `GET personnel/v1/employee-multi-phone-numbers` |  |
| [Get Employment Details](actions/get-employment-details.md) | `GET personnel/v1/employment-details` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details) |
| [Get Person Details](actions/get-person-details.md) | `GET personnel/v1/person-details` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details) |
| [Get Platform Configuration Fields](actions/get-platform-configuration-fields.md) | `GET personnel/v1/platform-configuration-fields/class-name/:className` |  |
| [Get User Defined Fields](actions/get-user-defined-fields.md) | `GET personnel/v1/user-defined-fields` |  |
| [Retrieve All Job Configurations](actions/retrieve-all-job-configurations.md) | `GET configuration/v1/jobs` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details) |
| [Retrieve All Locations Configurations](actions/retrieve-all-locations-configurations.md) | `GET configuration/v1/locations/` | [docs](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details) |
