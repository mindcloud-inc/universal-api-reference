# <img src="https://images.mindcloud.co/apps/icons/paycom_1782742380045.png" alt="Paycom logo" width="28" height="28"> Paycom: Universal API

Cloud-based human capital management (HCM) system that provides integrated payroll, human resources (HR), and talent management solutions, allowing businesses to manage their HR and payroll data in one place

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paycom/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paycom.com/
- **Vendor API docs:** https://drive.google.com/drive/folders/1Ug5PtxNyl2okfXJvsiZqWyqhZwS3XkBY?usp=sharing

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET |  |
| [List Employee Changed](actions/list-employee.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [List Employees Active](actions/list-employees-active.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Custom Fields](actions/get-employee-custom-fields.md) | GET |  |
| [Get Employee Effective Rate](actions/get-employee-effective-rate.md) | GET |  |
| [Get Employee New Hire](actions/get-employee-new-hire.md) | GET |  |
| [Get Employee Rate](actions/get-employee-rate.md) | GET |  |
| [Get Employee Sensitive](actions/get-employee-sensitive.md) | GET |  |
| [List Employee Changes](actions/list-employee-changes.md) | GET |  |
| [List Employee ids](actions/list-employees-ids.md) | GET |  |
| [List Employees Sensitive Changes](actions/list-employees-sensitive-changes.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Get Clocked In/Out Status](actions/get-clocked-in-out-status.md) | GET |  |
| [Get Punch Audit](actions/get-punch-audit.md) | GET | The Get method returns historical information for an employee's punches in a given date range. This method defaults to the current pay… |
| [Get Punch History](actions/get-punch-history.md) | GET |  |

