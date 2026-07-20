# <img src="https://images.mindcloud.co/apps/icons/craftboxx-icon_1775684996510.jpeg" alt="Craftboxx logo" width="28" height="28"> Craftboxx: Universal API

Craftboxx is field service and job-planning software for trades businesses, covering projects, assignments, customers, staff, time tracking, materials, tools, vehicles, and site documentation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/craftboxx/latest
- **Category:** Support / Field Service
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.craftboxx.de/
- **Vendor API docs:** https://api.craftboxx.de/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | POST | Creates and returns a Craftboxx access token. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates an article in Craftboxx. |
| [Get Article](actions/get-article.md) | GET | Returns a specific article from Craftboxx. |
| [List Articles](actions/list-articles.md) | GET | Returns articles from Craftboxx. |
| [Update Article](actions/update-article.md) | PUT | Updates an article in Craftboxx. |

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | POST | Creates an assignment in Craftboxx. |
| [Get Assignment](actions/get-assignment.md) | GET | Returns a specific assignment from Craftboxx. |
| [List Assignments](actions/list-assignments.md) | GET | Returns assignments from Craftboxx. |
| [Update Assignment](actions/update-assignment.md) | PUT | Updates an assignment in Craftboxx. |

### Assignment Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Assignment Availability](actions/check-assignment-availability.md) | GET | Returns unavailable assignment master data for a date range from Craftboxx. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Craftboxx. |
| [Get Customer](actions/get-customer.md) | GET | Returns a specific customer from Craftboxx. |
| [List Customers](actions/list-customers.md) | GET | Returns customers from Craftboxx. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Craftboxx. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST | Creates an employee in Craftboxx. |
| [Get Employee](actions/get-employee.md) | GET | Returns a specific employee from Craftboxx. |
| [List Employees](actions/list-employees.md) | GET | Returns employees from Craftboxx. |
| [Update Employee](actions/update-employee.md) | PUT | Updates an employee in Craftboxx. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Craftboxx. |
| [Get Project](actions/get-project.md) | GET | Returns a specific project from Craftboxx. |
| [List Projects](actions/list-projects.md) | GET | Returns projects from Craftboxx. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Craftboxx. |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST | Creates a timesheet in Craftboxx. |
| [Get Timesheet](actions/get-timesheet.md) | GET | Returns a specific timesheet from Craftboxx. |
| [List Timesheets](actions/list-timesheets.md) | GET | Returns timesheets from Craftboxx. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates a timesheet in Craftboxx. |

