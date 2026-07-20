# <img src="https://images.mindcloud.co/apps/icons/leave-dates_1774881850533.png" alt="Leave Dates logo" width="28" height="28"> Leave Dates: Universal API

Manage staff leave, calendars, and time off requests

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leaveDates/latest
- **Category:** Human Resources / HRIS
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leavedates.com
- **Vendor API docs:** https://api.leavedates.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Allowance Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Allowance Type](actions/create-allowance-type.md) | POST | Creates a new allowance type in Leave Dates. |
| [Delete Allowance Type](actions/delete-allowance-type.md) | DELETE | Deletes an existing allowance type from Leave Dates. |
| [Get Allowance Type](actions/get-allowance-type.md) | GET | Retrieves an allowance type from Leave Dates. |
| [List Allowance Types](actions/list-allowance-types.md) | GET | Retrieves allowance types for a company in Leave Dates. |
| [Update Allowance Type](actions/update-allowance-type.md) | PUT | Updates an existing allowance type in Leave Dates. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies available to the authenticated user in Leave Dates. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves country names from Leave Dates. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Add Department](actions/add-department.md) | POST | Creates a new department in Leave Dates. |
| [Delete Department](actions/delete-department.md) | DELETE | Deletes an existing department from Leave Dates. |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments for a company in Leave Dates. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in Leave Dates. |

### Employment

| Action | Method | Description |
| --- | --- | --- |
| [Add Employment](actions/add-employment.md) | POST | Creates a new employment in Leave Dates. |
| [Delete Employment](actions/delete-employment.md) | DELETE | Deletes an existing employment from Leave Dates. |
| [Get Employment](actions/get-employment.md) | GET | Retrieves employment details from Leave Dates. |
| [List Employments](actions/list-employments.md) | GET | Retrieves employment records for a company in Leave Dates. |
| [Update Employment](actions/update-employment.md) | PUT | Updates an existing employment in Leave Dates. |

### Employment Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Employment Report](actions/get-employment-report.md) | GET | Retrieves employment report rows from Leave Dates. |

### Leave Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Type](actions/create-leave-type.md) | POST | Creates a new leave type in Leave Dates. |
| [Delete Leave Type](actions/delete-leave-type.md) | DELETE | Deletes an existing leave type from Leave Dates. |
| [List Leave Types](actions/list-leave-types.md) | GET | Retrieves leave types for a company in Leave Dates. |
| [Update Leave Type](actions/update-leave-type.md) | PUT | Updates an existing leave type in Leave Dates. |

