# TimeLive: Native API Reference

A consolidated summary of TimeLive's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://livetecs.com/timelive/integrations/
- **API base URL:** `https://mindcloudtl.livetecs.com/classic/api`

## Authentication

### Bearer Access Token

Authenticate to a tenant-specific TimeLive account with an access token. Keep the account employee id available for scoped requests and validation flows.

### Credentials

- **API Key:** `apiKey` · required
- **Account Employee Id:** `accountEmployeeId` · required · Account employee id kept available for employee-scoped validation and request flows.

Send these headers with each API request:

```http
AccessToken: <apiKey>
```

[Official authentication documentation](https://livetecs.com/timelive/release-notes/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | `GET /Clients` | [docs](https://livetecs.com/timelive/integrations/) |
| [List Employees](actions/list-employees.md) | `GET /Employees` | [docs](https://livetecs.com/timelive/integrations/) |
| [List Expenses](actions/list-expenses.md) | `GET /Expenses` | [docs](https://livetecs.com/timelive/integrations/) |
| [List Projects](actions/list-projects.md) | `GET /Projects` | [docs](https://livetecs.com/timelive/integrations/) |
| [List Tasks](actions/list-tasks.md) | `GET /Tasks` | [docs](https://livetecs.com/timelive/integrations/) |
| [List Time Entries By Employee Id And Date Range](actions/list-time-entries-by-employee-id-and-date-range.md) | `GET /Timesheets/TimeEntriesByEmployeeIdAndDateRange/:employeeId/:startDate/:endDate` | [docs](https://livetecs.com/timelive/release-notes/) |
