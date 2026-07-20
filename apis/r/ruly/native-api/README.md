# Ruly: Native API Reference

A consolidated summary of Ruly's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/
- **API base URL:** `https://mindcloud.api.rulyapp.com`

## Authentication

### API token

Use a Ruly API token for authenticated API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Employee Record](actions/create-employee-record.md) | `POST data/employee/` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Delete Employee Record](actions/delete-employee-record.md) | `DELETE data/employee/:employeeId` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Get Employee](actions/get-employee.md) | `GET data/employee/:employeeId` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Get Employee Records with Specific Fields](actions/get-employee-records-with-specific-fields.md) | `GET data/employee/` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Get Filtered Employee Records](actions/get-filtered-employee-records.md) | `GET data/employee/` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Get Linked Records from Employee](actions/get-linked-records-from-employee.md) | `GET data/employee/:employeeId` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [List Employees](actions/list-employees.md) | `GET data/employee/` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [List Employees Sorted by Last Name](actions/list-employees-sorted-by-last-name.md) | `GET data/employee/` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
| [Update Employee City](actions/update-employee-city.md) | `PUT data/employee/:employeeId` | [docs](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/) |
