# DeskTime: Native API Reference

A consolidated summary of DeskTime's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://help.desktime.com/hc/en-us/sections/25494426310045
- **API base URL:** `https://desktime.com/api/v2/json`

## Authentication

### DeskTime API Key

Use your DeskTime API key to authenticate requests to the DeskTime API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.desktime.com/hc/en-us/articles/25494558790685-What-is-API)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /create-project` | [docs](https://help.desktime.com/hc/en-us/articles/25495264299293-How-to-create-a-project-with-API) |
| [Get Company Account](actions/get-company-account.md) | `GET /company` | [docs](https://help.desktime.com/hc/en-us/articles/25494763327901-How-to-use-Account-endpoint) |
| [Get Employee](actions/get-employee.md) | `GET /employee` | [docs](https://help.desktime.com/hc/en-us/articles/25494877861789-How-to-get-employee-data-with-API) |
| [Get Employee Apps](actions/get-employee-apps.md) | `GET /employee/apps` | [docs](https://help.desktime.com/hc/en-us/articles/25494932087709-How-to-get-employee-apps-data-with-API) |
| [Get Employee Projects](actions/get-employee-projects.md) | `GET /employee/projects` | [docs](https://help.desktime.com/hc/en-us/articles/25494912262301-How-to-get-employee-projects-data-with-API) |
| [Get Employee Projects and Apps](actions/get-employee-projects-and-apps.md) | `GET /employee/basic` | [docs](https://help.desktime.com/hc/en-us/articles/25494997505053-How-to-get-employee-projects-and-apps-data-with-API) |
| [List Company Employees](actions/list-company-employees.md) | `GET /employees` | [docs](https://help.desktime.com/hc/en-us/articles/25495139812637-How-to-get-all-company-employees-with-API) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://help.desktime.com/hc/en-us/articles/25495195415453-How-to-get-projects-with-API) |
| [Ping API](actions/ping-api.md) | `GET /ping` | [docs](https://help.desktime.com/hc/en-us/articles/25494685459357-How-to-use-ping-request) |
| [Start Project and Task Tracking](actions/start-project-and-task-tracking.md) | `GET /start-project` | [docs](https://help.desktime.com/hc/en-us/articles/25495406925853-How-to-start-a-project-and-task-with-API) |
| [Stop Project and Task Tracking](actions/stop-project-and-task-tracking.md) | `GET /stop-project` | [docs](https://help.desktime.com/hc/en-us/articles/25495406925853-How-to-start-a-project-and-task-with-API) |
