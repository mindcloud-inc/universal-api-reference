# <img src="https://images.mindcloud.co/apps/icons/deputy_1773771693125.png" alt="Deputy logo" width="28" height="28"> Deputy: Universal API

Schedule staff, track time, and manage leave with Deputy

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deputy/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deputy.com
- **Vendor API docs:** https://developer.deputy.com/docs/getting-started-with-the-deputy-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a single contact from Deputy. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves the contact list from Deputy. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds matching contact records in Deputy. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves the country list from Deputy. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a single custom field from Deputy. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves the custom field list from Deputy. |
| [Search Custom Fields](actions/search-custom-fields.md) | GET | Finds matching custom fields in Deputy. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST | Creates a new employee in Deputy. |
| [Get Employee](actions/get-employee.md) | GET | Retrieves a single employee from Deputy. |
| [List Employees](actions/list-employees.md) | GET | Retrieves the employee list from Deputy. |
| [Search Employees](actions/search-employees.md) | GET | Finds matching employee records in Deputy. |

### Employee Pay Condition

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Pay Conditions](actions/list-employee-pay-conditions.md) | GET | Retrieves employee pay conditions from Deputy. |

### Labor Model Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Labor Model Rules](actions/list-labor-model-rules.md) | GET | Retrieves labor model rules from Deputy. |

### Leave Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Request](actions/create-leave-request.md) | POST | Creates a new leave request in Deputy. |
| [Get Leave Request](actions/get-leave-request.md) | GET | Retrieves a single leave request from Deputy. |
| [List Leave Requests](actions/list-leave-requests.md) | GET | Retrieves the leave request list from Deputy. |
| [Search Leave Requests](actions/search-leave-requests.md) | GET | Finds matching leave requests in Deputy. |

### Sales Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Data](actions/list-sales-data.md) | GET | Retrieves raw sales metrics from Deputy. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Add Shift](actions/add-shift.md) | POST | Creates a new shift in Deputy. |
| [List Shifts](actions/list-shifts.md) | GET | Retrieves the shift list from Deputy. |

### State

| Action | Method | Description |
| --- | --- | --- |
| [List States](actions/list-states.md) | GET | Retrieves the state list from Deputy. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Get Timesheet Details](actions/get-timesheet-details.md) | GET | Retrieves detailed timesheet data from Deputy. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves the timesheet list from Deputy. |

### Timesheet Pay Return

| Action | Method | Description |
| --- | --- | --- |
| [List Timesheet Pay Returns](actions/list-timesheet-pay-returns.md) | GET | Retrieves timesheet pay returns from Deputy. |

