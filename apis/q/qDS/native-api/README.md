# QDS: Native API Reference

A consolidated summary of QDS's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://qdsapp.com/api/docs
- **API base URL:** `https://qdsapp.com/api/v1`

## Authentication

### Personal Access Token

Connect QDS with a personal access token generated from My Account > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.qualitydrivensoftware.com/support/solutions/articles/9000182019-service-autopilot-automated-qds-surveys)

## API conventions

Response data is read from `roles`.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` |  |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` |  |
| [Get Client](actions/get-client.md) | `GET /clients/:clientId` | [docs](https://qdsapp.com/api/docs) |
| [Get Current User](actions/get-current-user.md) | `GET /user/current` |  |
| [Get Dashboard Report](actions/get-dashboard-report.md) | `GET /reports/dashboard` |  |
| [Get Employee](actions/get-employee.md) | `GET /employees/:employeeId` | [docs](https://qdsapp.com/api/docs) |
| [Get Issue](actions/get-issue.md) | `GET /issues/:issueId` |  |
| [Get Survey](actions/get-survey.md) | `GET /surveys/:surveyId` |  |
| [List Active Complaint Issues](actions/list-active-complaint-issues.md) | `GET /complaintissues/active` |  |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://qdsapp.com/api/docs) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://qdsapp.com/api/docs) |
| [List Issues](actions/list-issues.md) | `GET /issues` |  |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` |  |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` |  |
| [List Roles](actions/list-roles.md) | `GET /roles` |  |
| [List Survey Templates](actions/list-survey-templates.md) | `GET /surveytemplates` |  |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` |  |
| [Update Client](actions/update-client.md) | `PUT /clients/:clientId` |  |
