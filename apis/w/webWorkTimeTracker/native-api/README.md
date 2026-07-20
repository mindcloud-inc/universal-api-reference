# WebWork Time Tracker: Native API Reference

A consolidated summary of WebWork Time Tracker's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.webwork-tracker.com
- **API base URL:** `https://api.webwork-tracker.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.webwork-tracker.com/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.pagination.last_page`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Time Request](actions/approve-time-request.md) | `POST /time-requests/:timeRequestId/approve` | [docs](https://api-docs.webwork-tracker.com/api/time-requests/approvetimerequest) |
| [Archive Member](actions/archive-member.md) | `DELETE /members/:memberId` | [docs](https://api-docs.webwork-tracker.com/api/members/deletemember) |
| [Archive Project](actions/archive-project.md) | `DELETE /projects/:projectId` | [docs](https://api-docs.webwork-tracker.com/api/projects/deleteproject) |
| [Assign Task to User](actions/assign-task-to-user.md) | `POST /tasks/:taskId/assign/:userId` | [docs](https://api-docs.webwork-tracker.com/api/tasks/assigntask) |
| [Create Contract](actions/create-contract.md) | `POST /contracts` | [docs](https://api-docs.webwork-tracker.com/api/contracts/createcontract) |
| [Create Expense](actions/create-expense.md) | `POST /expenses` | [docs](https://api-docs.webwork-tracker.com/api/expenses/createexpense) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api-docs.webwork-tracker.com/api/projects/createproject) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://api-docs.webwork-tracker.com/api/tasks/createtask) |
| [Create Time Request](actions/create-time-request.md) | `POST /time-requests` | [docs](https://api-docs.webwork-tracker.com/api/time-requests/createtimerequest) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://api-docs.webwork-tracker.com/api/tasks/deletetask) |
| [Get Contract](actions/get-contract.md) | `GET /contracts/:contractId` | [docs](https://api-docs.webwork-tracker.com/api/contracts/getcontract) |
| [Get Member](actions/get-member.md) | `GET /members/:memberId` | [docs](https://api-docs.webwork-tracker.com/api/members/getmember) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://api-docs.webwork-tracker.com/api/projects/getproject) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://api-docs.webwork-tracker.com/api/tasks/gettask) |
| [Get Tracked Hours Report](actions/get-tracked-hours-report.md) | `GET /reports/tracked-hours` | [docs](https://api-docs.webwork-tracker.com/api/reports/gettrackedhoursreport) |
| [Invite Member](actions/invite-member.md) | `POST /members` | [docs](https://api-docs.webwork-tracker.com/api/members/invitemember) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://api-docs.webwork-tracker.com/api/contracts/getcontracts) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://api-docs.webwork-tracker.com/api/expenses/getexpenses) |
| [List Leave Balances](actions/list-leave-balances.md) | `GET /leaves/balances` | [docs](https://api-docs.webwork-tracker.com/api/leaves/getleavebalances) |
| [List Leaves](actions/list-leaves.md) | `GET /leaves` | [docs](https://api-docs.webwork-tracker.com/api/leaves/getleaves) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://api-docs.webwork-tracker.com/api/members/getmembers) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api-docs.webwork-tracker.com/api/projects/getprojects) |
| [List Task Assignees](actions/list-task-assignees.md) | `GET /tasks/:taskId/assignees` | [docs](https://api-docs.webwork-tracker.com/api/tasks/gettaskassignees) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://api-docs.webwork-tracker.com/api/tasks/gettasks) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time-entries` | [docs](https://api-docs.webwork-tracker.com/api/time-entries/gettimeentries) |
| [List Time Requests](actions/list-time-requests.md) | `GET /time-requests` | [docs](https://api-docs.webwork-tracker.com/api/time-requests/gettimerequests) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets` | [docs](https://api-docs.webwork-tracker.com/api/timesheets/gettimesheets) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://api-docs.webwork-tracker.com/api/workspaces/getworkspaces) |
| [Reject Time Request](actions/reject-time-request.md) | `POST /time-requests/:timeRequestId/reject` | [docs](https://api-docs.webwork-tracker.com/api/time-requests/rejecttimerequest) |
| [Start Time Tracking](actions/start-time-tracking.md) | `POST /time-tracking/start` | [docs](https://api-docs.webwork-tracker.com/api/time-tracking/starttimetracking) |
| [Stop Time Tracking](actions/stop-time-tracking.md) | `POST /time-tracking/stop` | [docs](https://api-docs.webwork-tracker.com/api/time-tracking/stoptimetracking) |
| [Unassign Task from User](actions/unassign-task-from-user.md) | `DELETE /tasks/:taskId/unassign/:userId` | [docs](https://api-docs.webwork-tracker.com/api/tasks/unassigntask) |
| [Update Contract](actions/update-contract.md) | `PUT /contracts/:contractId` | [docs](https://api-docs.webwork-tracker.com/api/contracts/updatecontract) |
| [Update Member](actions/update-member.md) | `PUT /members/:memberId` | [docs](https://api-docs.webwork-tracker.com/api/members/updatemember) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectId` | [docs](https://api-docs.webwork-tracker.com/api/projects/updateproject) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://api-docs.webwork-tracker.com/api/tasks/updatetask) |
