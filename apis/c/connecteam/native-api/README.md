# Connecteam: Native API Reference

A consolidated summary of Connecteam's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developer.connecteam.com/docs/introduction-1
- **API base URL:** `https://api.connecteam.com`

## Authentication

### API Key

Authenticate with a Connecteam API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.connecteam.com/docs/authentication-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Jobs](actions/create-jobs.md) | `POST /jobs/v1/jobs` | [docs](https://developer.connecteam.com/reference/create_jobs_jobs_v1_jobs_post) |
| [Create Task](actions/create-task.md) | `POST /tasks/v1/taskboards/:taskBoardId/tasks` | [docs](https://developer.connecteam.com/reference/create_task_tasks_v1_taskboards__taskBoardId__tasks_post) |
| [Create Time Off Request](actions/create-time-off-request.md) | `POST /time-off/v1/requests` | [docs](https://developer.connecteam.com/reference/post_time_off_request_time_off_v1_requests_post) |
| [Create Users](actions/create-users.md) | `POST /users/v1/users` | [docs](https://developer.connecteam.com/reference/create_users_users_v1_users_post) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/v1/jobs/:jobId` | [docs](https://developer.connecteam.com/reference/delete_job_jobs_v1_jobs__jobId__delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/v1/taskboards/:taskBoardId/tasks/:taskId` | [docs](https://developer.connecteam.com/reference/delete_task_tasks_v1_taskboards__taskBoardId__tasks__taskId__delete) |
| [Get Account Information](actions/get-account-information.md) | `GET /me` | [docs](https://developer.connecteam.com/reference/get_account_information_me_get) |
| [Get Job](actions/get-job.md) | `GET /jobs/v1/jobs/:jobId` | [docs](https://developer.connecteam.com/reference/get_job_jobs_v1_jobs__jobId__get) |
| [Get Timesheet Totals](actions/get-timesheet-totals.md) | `GET /time-clock/v1/time-clocks/:timeClockId/timesheet` | [docs](https://developer.connecteam.com/reference/get_timesheet_total_hours_time_clock_v1_time_clocks__timeClockId__timesheet_get) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /users/v1/custom-fields` | [docs](https://developer.connecteam.com/reference/get_custom_fields_users_v1_custom_fields_get) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs/v1/jobs` | [docs](https://developer.connecteam.com/reference/get_jobs_jobs_v1_jobs_get) |
| [List Policy Types](actions/list-policy-types.md) | `GET /time-off/v1/policy-types` | [docs](https://developer.connecteam.com/reference/get_policy_groups_time_off_v1_policy_types_get) |
| [List Task Boards](actions/list-task-boards.md) | `GET /tasks/v1/taskboards` | [docs](https://developer.connecteam.com/reference/get_tasks_boards_tasks_v1_taskboards_get) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks/v1/taskboards/:taskBoardId/tasks` | [docs](https://developer.connecteam.com/reference/get_tasks_tasks_v1_taskboards__taskBoardId__tasks_get) |
| [List Time Activities](actions/list-time-activities.md) | `GET /time-clock/v1/time-clocks/:timeClockId/time-activities` | [docs](https://developer.connecteam.com/reference/get_time_activities_time_clock_v1_time_clocks__timeClockId__time_activities_get) |
| [List Time Clocks](actions/list-time-clocks.md) | `GET /time-clock/v1/time-clocks` | [docs](https://developer.connecteam.com/reference/get_time_clocks_time_clock_v1_time_clocks_get) |
| [List User Balances](actions/list-user-balances.md) | `GET /time-off/v1/policy-types/:policyTypeId/balances` | [docs](https://developer.connecteam.com/reference/get_balances_time_off_v1_policy_types__policyTypeId__balances_get) |
| [List User Unavailabilities](actions/list-user-unavailabilities.md) | `GET /scheduler/v1/schedulers/user-unavailability` | [docs](https://developer.connecteam.com/reference/get_unavailabilities_scheduler_v1_schedulers_user_unavailability_get) |
| [List Users](actions/list-users.md) | `GET /users/v1/users` | [docs](https://developer.connecteam.com/reference/get_users_users_v1_users_get) |
| [Update Job](actions/update-job.md) | `PUT /jobs/v1/jobs/:jobId` | [docs](https://developer.connecteam.com/reference/update_job_jobs_v1_jobs__jobId__put) |
| [Update Task](actions/update-task.md) | `PUT /tasks/v1/taskboards/:taskBoardId/tasks/:taskId` | [docs](https://developer.connecteam.com/reference/update_task_tasks_v1_taskboards__taskBoardId__tasks__taskId__put) |
| [Update Users](actions/update-users.md) | `PUT /users/v1/users` | [docs](https://developer.connecteam.com/reference/edit_users_users_v1_users_put) |
