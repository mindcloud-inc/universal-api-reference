# <img src="https://images.mindcloud.co/apps/icons/paylocity-icon_1782394126500.png" alt="Paylocity logo" width="28" height="28"> Paylocity: Universal API

All-in-one Modern HR and Payroll Software

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paylocity/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET | Retrieves the list of employees of a company |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Information](actions/get-company-information.md) | GET |  |
| [Get Company Shifts](actions/get-company-shifts.md) | GET |  |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee Punch](actions/create-employee-punch.md) | POST |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Punch Detail](actions/get-employee-punch-detail.md) | GET |  |
| [Get Employee Shifts](actions/get-employee-shifts.md) | GET |  |

