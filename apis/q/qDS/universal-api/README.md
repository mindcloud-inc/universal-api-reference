# <img src="https://images.mindcloud.co/apps/icons/q-ds_1774455859130.png" alt="QDS logo" width="28" height="28"> QDS: Universal API

Manage clients, surveys, employees, and service quality in QDS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qDS/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qualitydrivensoftware.com
- **Vendor API docs:** https://qdsapp.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Roles](actions/list-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from QDS by ID. |
| [List Clients](actions/list-clients.md) | GET | Retrieves a list of clients from QDS. |
| [Update Client](actions/update-client.md) | PUT |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from QDS by ID. |
| [List Employees](actions/list-employees.md) | GET | Retrieves a list of employees from QDS. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue](actions/get-issue.md) | GET |  |
| [List Active Complaint Issues](actions/list-active-complaint-issues.md) | GET |  |
| [List Issues](actions/list-issues.md) | GET |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Report](actions/get-dashboard-report.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET |  |
| [List Reviews](actions/list-reviews.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Templates](actions/list-survey-templates.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

