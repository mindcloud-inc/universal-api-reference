# <img src="https://images.mindcloud.co/apps/icons/desk-time_1774389829984.png" alt="DeskTime logo" width="28" height="28"> DeskTime: Universal API

DeskTime is an all-in-one time tracker for remote, hybrid, and in-office teams, with project tracking, employee activity data, and productivity reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deskTime/latest
- **Category:** Productivity / Project Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://desktime.com
- **Vendor API docs:** https://help.desktime.com/hc/en-us/sections/25494426310045

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Account](actions/get-company-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Api Health

| Action | Method | Description |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | GET | Checks whether the DeskTime API is responding. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Account](actions/get-company-account.md) | GET | Retrieves your company account details from DeskTime. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves employee tracking data from DeskTime for a specific date. |
| [Get Employee Apps](actions/get-employee-apps.md) | GET | Retrieves an employee's tracked apps from DeskTime for a date. |
| [Get Employee Projects](actions/get-employee-projects.md) | GET | Retrieves an employee's tracked projects from DeskTime for a date. |
| [Get Employee Projects and Apps](actions/get-employee-projects-and-apps.md) | GET | Retrieves an employee's tracked projects and apps from DeskTime. |
| [List Company Employees](actions/list-company-employees.md) | GET | Retrieves company employees from DeskTime for a day or month. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in DeskTime with an optional task. |
| [List Projects](actions/list-projects.md) | GET | Retrieves active projects from DeskTime with their tasks. |
| [Start Project and Task Tracking](actions/start-project-and-task-tracking.md) | PUT | Starts time tracking for a DeskTime project and task. |
| [Stop Project and Task Tracking](actions/stop-project-and-task-tracking.md) | PUT | Stops time tracking for a DeskTime project and task. |

