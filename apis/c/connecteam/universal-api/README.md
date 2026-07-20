# <img src="https://images.mindcloud.co/apps/icons/c64558b-ct-favicon_1773255072555.png" alt="Connecteam logo" width="28" height="28"> Connecteam: Universal API

Manage employees, schedules, time tracking, tasks, and team communication

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/connecteam/latest
- **Category:** Human Resources / HRIS
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://connecteam.com
- **Vendor API docs:** https://developer.connecteam.com/docs/introduction-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Jobs](actions/create-jobs.md) | POST | Create individual or multiple jobs under a specified scheduler |
| [Delete Job](actions/delete-job.md) | DELETE | Delete a single job by its unique identifier. Currently, deleting a sub-job and/or job with nested sub-jobs is not supported. |
| [Get Job](actions/get-job.md) | GET | Retrieve a single job information by its unique ID |
| [List Jobs](actions/list-jobs.md) | GET | Get a list of job objects relevant to instance id (scheduler id or time clock id). If unified jobs are disabled, only schedulers are… |
| [Update Job](actions/update-job.md) | PUT | Update a single job by its unique identifier. Currently, updating job with nested sub-jobs is not supported. |

### Scheduler

| Action | Method | Description |
| --- | --- | --- |
| [List User Unavailabilities](actions/list-user-unavailabilities.md) | GET | Retrieve a list of user unavailabilities, approved time-off requests and assigned shifts |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Create quick task for specified users by their ID, detailing information such as title, due date and description. Attachments for the quick… |
| [Delete Task](actions/delete-task.md) | DELETE | Delete quick task under a specified task board |
| [List Task Boards](actions/list-task-boards.md) | GET | Retrieve a list of task boards associated with the account |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks under a specified task board |
| [Update Task](actions/update-task.md) | PUT | Update a quick task under a specified task board. Any new attachments will replace the existing ones. |

### Time Clock

| Action | Method | Description |
| --- | --- | --- |
| [Get Timesheet Totals](actions/get-timesheet-totals.md) | GET | Retrieves detailed work records for each employee within a specified date range. This endpoint is designed to support payroll processing by… |
| [List Time Activities](actions/list-time-activities.md) | GET | Retrieve a list of time activities in under a specified time clock. Time activities include shift and/or manual breaks |
| [List Time Clocks](actions/list-time-clocks.md) | GET | Retrieve a list of time clocks associated with the account |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Off Request](actions/create-time-off-request.md) | POST | Create a new time-off request for a user under a specified policy. The time-off request can be either in pending or approved status. |
| [List Policy Types](actions/list-policy-types.md) | GET | Retrieve a list of policy types associated with the account |
| [List User Balances](actions/list-user-balances.md) | GET | Retrieve a list of user time-off balances within a policy type |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Users](actions/create-users.md) | POST | Create individual or multiple users associated with the account using the provided details. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves all custom fields associated with the account. Optionally, filter the results by categories, names, types, or custom field IDs. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of all users associated with the account. Optionally, filter by user ID to receive specific user information |
| [Update Users](actions/update-users.md) | PUT | Update individual or multiple users associated with the account using the provided details. You can specify updates either by their phone… |

