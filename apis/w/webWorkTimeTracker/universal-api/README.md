# <img src="https://images.mindcloud.co/apps/icons/web-work-time-tracker_1774987462618.png" alt="WebWork Time Tracker logo" width="28" height="28"> WebWork Time Tracker: Universal API

Track time, manage tasks, and automate payroll

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webWorkTimeTracker/latest
- **Category:** Productivity / Project Management
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webwork-tracker.com
- **Vendor API docs:** https://api-docs.webwork-tracker.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates an expense in WebWork Time Tracker. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from WebWork Time Tracker. |

### Leave Balance

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Balances](actions/list-leave-balances.md) | GET | Retrieves leave balances from WebWork Time Tracker. |

### Leave Request

| Action | Method | Description |
| --- | --- | --- |
| [List Leaves](actions/list-leaves.md) | GET | Retrieves leaves from WebWork Time Tracker. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Archive Member](actions/archive-member.md) | DELETE | Archives a member in WebWork Time Tracker. |
| [Archive Project](actions/archive-project.md) | DELETE | Archives a project in WebWork Time Tracker. |
| [Create Contract](actions/create-contract.md) | POST | Creates a new contract in WebWork Time Tracker. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in WebWork Time Tracker. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in WebWork Time Tracker. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from WebWork Time Tracker. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from WebWork Time Tracker. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from WebWork Time Tracker. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from WebWork Time Tracker. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from WebWork Time Tracker. |
| [Invite Member](actions/invite-member.md) | POST | Invites a new member to WebWork Time Tracker. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves workspace contracts from WebWork Time Tracker. |
| [List Members](actions/list-members.md) | GET | Retrieves workspace members from WebWork Time Tracker. |
| [List Projects](actions/list-projects.md) | GET | Retrieves workspace projects from WebWork Time Tracker. |
| [List Task Assignees](actions/list-task-assignees.md) | GET | Retrieves task assignees from WebWork Time Tracker. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves project tasks from WebWork Time Tracker. |
| [Update Contract](actions/update-contract.md) | PUT | Updates an existing contract in WebWork Time Tracker. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in WebWork Time Tracker. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in WebWork Time Tracker. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in WebWork Time Tracker. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Assign Task to User](actions/assign-task-to-user.md) | PUT | Assigns a task to a user in WebWork Time Tracker. |
| [Unassign Task from User](actions/unassign-task-from-user.md) | PUT | Unassigns a user from a task in WebWork Time Tracker. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from WebWork Time Tracker. |

### Time Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Request](actions/create-time-request.md) | POST | Creates a time request in WebWork Time Tracker. |
| [List Time Requests](actions/list-time-requests.md) | GET | Retrieves time requests from WebWork Time Tracker. |

### Time Request Approval

| Action | Method | Description |
| --- | --- | --- |
| [Approve Time Request](actions/approve-time-request.md) | PUT | Approves a time request in WebWork Time Tracker. |
| [Reject Time Request](actions/reject-time-request.md) | PUT | Rejects a time request in WebWork Time Tracker. |

### Time Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Start Time Tracking](actions/start-time-tracking.md) | POST | Starts time tracking in WebWork Time Tracker. |
| [Stop Time Tracking](actions/stop-time-tracking.md) | PUT | Stops time tracking in WebWork Time Tracker. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from WebWork Time Tracker. |

### Tracked Hours Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracked Hours Report](actions/get-tracked-hours-report.md) | GET | Retrieves tracked hours reports from WebWork Time Tracker. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from WebWork Time Tracker. |

