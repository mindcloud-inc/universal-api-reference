# <img src="https://images.mindcloud.co/apps/icons/u-kgready-icon_1782394617480.jpg" alt="UKG Ready logo" width="28" height="28"> UKG Ready: Universal API

UKG Ready through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uKGReady/latest
- **Category:** Human Resources / HRIS
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://secure7.saashr.com/ta/docs/rest/public/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Centers](actions/list-cost-centers.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Assignments](actions/get-account-assignments.md) | GET |  |
| [Get Employee](actions/get-employee.md) | GET |  |
| [Get Employee Attendance](actions/get-employee-attendance.md) | GET |  |
| [Get Employee Badges](actions/get-employee-badges.md) | GET |  |
| [Get Employee Contact](actions/get-employee-contact.md) | GET |  |
| [Get Employee Demographics](actions/get-employee-demographics.md) | GET |  |
| [Get Employee Detail](actions/get-employee-detail.md) | GET |  |
| [Get Employee Pay Info](actions/get-employee-pay-info.md) | GET |  |
| [Get Employee Profiles](actions/get-employee-profiles.md) | GET |  |
| [List Employee Time Entries](actions/list-employee-time-entries.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Compensation per company](actions/get-compensation-per-company.md) | GET |  |

### Payrolls

| Action | Method | Description |
| --- | --- | --- |
| [Get Pay Types](actions/get-pay-types.md) | GET |  |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Punches](actions/create-time-punches.md) | POST |  |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE |  |
| [List Time Entries](actions/list-time-entries.md) | GET |  |
| [Update Time Entries](actions/update-time-entries.md) | PUT |  |

