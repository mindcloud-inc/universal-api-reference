# OfficeClip: Native API Reference

A consolidated summary of OfficeClip's API configuration and 92 documented operations, with links to official documentation.

- **Official docs:** https://app.officeclip.com/swagger/ui/index
- **OpenAPI specification:** https://app.officeclip.com/swagger/docs/v1
- **API base URL:** `https://app.officeclip.com`

## Authentication

### API Key

Authenticate OfficeClip with an API key and Org key.

### Credentials

- **API Key:** `apiKey` · required
- **Org Key:** `orgKey` · required · OfficeClip organization key from Rest API Integration.

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
X-OrgKey: <orgKey>
```

[Official authentication documentation](https://www.officeclip.com/help/apps/integration/zapier.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (92 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account Detail](actions/create-account-detail.md) | `POST /api/account-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Contact Detail](actions/create-contact-detail.md) | `POST /api/contact-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Event Detail](actions/create-event-detail.md) | `POST /api/event-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Expense](actions/create-expense.md) | `POST /api/expense-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Expense Detail](actions/create-expense-detail.md) | `POST /api/expense-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Image Detail](actions/create-image-detail.md) | `POST /api/image-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Note](actions/create-note.md) | `POST /api/note` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Note Detail](actions/create-note-detail.md) | `POST /api/note-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Notebook](actions/create-notebook.md) | `POST /api/notebook` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Sub Task](actions/create-sub-task.md) | `POST /api/subtask` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Task Detail](actions/create-task-detail.md) | `POST /api/task-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Time Off Detail](actions/create-time-off-detail.md) | `POST /api/timeoff-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Timesheet](actions/create-timesheet.md) | `POST /api/timesheet-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Timesheet Detail](actions/create-timesheet-detail.md) | `POST /api/timesheet-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Tracker Case Detail](actions/create-tracker-case-detail.md) | `POST /api/tracker-case-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Create Workflow Summary](actions/create-workflow-summary.md) | `POST /api/workflow-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Account Detail](actions/delete-account-detail.md) | `DELETE /api/account-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Contact Detail](actions/delete-contact-detail.md) | `DELETE /api/contact-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Event Detail](actions/delete-event-detail.md) | `DELETE /api/event-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Expense](actions/delete-expense.md) | `DELETE /api/expense-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Expense Detail](actions/delete-expense-detail.md) | `DELETE /api/expense-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Note](actions/delete-note.md) | `DELETE /api/note/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Note Detail](actions/delete-note-detail.md) | `DELETE /api/note-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Notebook](actions/delete-notebook.md) | `DELETE /api/notebook/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Sub Task](actions/delete-sub-task.md) | `DELETE /api/subtask/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Task Detail](actions/delete-task-detail.md) | `DELETE /api/task-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Time Off Detail](actions/delete-time-off-detail.md) | `DELETE /api/timeoff-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Timesheet](actions/delete-timesheet.md) | `DELETE /api/timesheet-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Timesheet Detail](actions/delete-timesheet-detail.md) | `DELETE /api/timesheet-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Delete Tracker Case Detail](actions/delete-tracker-case-detail.md) | `DELETE /api/tracker-case-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Account Detail](actions/get-account-detail.md) | `GET /api/account-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Contact Detail](actions/get-contact-detail.md) | `GET /api/contact-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Event Detail](actions/get-event-detail.md) | `GET /api/event-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Expense](actions/get-expense.md) | `GET /api/expense-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Expense Detail](actions/get-expense-detail.md) | `GET /api/expense-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Image Detail](actions/get-image-detail.md) | `GET /api/image-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Note](actions/get-note.md) | `GET /api/note/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Note Detail](actions/get-note-detail.md) | `GET /api/note-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Profile Lists](actions/get-profile-lists.md) | `GET /api/profile-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Task Detail](actions/get-task-detail.md) | `GET /api/task-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Task Detail by Query ID](actions/get-task-detail-by-query-id.md) | `GET /api/task-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Time Off Detail](actions/get-time-off-detail.md) | `GET /api/timeoff-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Timesheet](actions/get-timesheet.md) | `GET /api/timesheet-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Timesheet Detail](actions/get-timesheet-detail.md) | `GET /api/timesheet-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Get Tracker Case Detail](actions/get-tracker-case-detail.md) | `GET /api/tracker-case-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Account Children](actions/list-account-children.md) | `GET /api/account-children` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Account Lists](actions/list-account-lists.md) | `GET /api/account-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Accounts](actions/list-accounts.md) | `GET /api/account-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Contact Children](actions/list-contact-children.md) | `GET /api/contact-children` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /api/contact-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Contacts](actions/list-contacts.md) | `GET /api/contact-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Event Lists](actions/list-event-lists.md) | `GET /api/event-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Events](actions/list-events.md) | `GET /api/event-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Expense Details](actions/list-expense-details.md) | `GET /api/expense-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Expense Group Profiles](actions/list-expense-group-profiles.md) | `GET /api/expense-group-profile` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Expense Lists](actions/list-expense-lists.md) | `GET /api/expense-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Expenses](actions/list-expenses.md) | `GET /api/expense-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Note Details](actions/list-note-details.md) | `GET /api/note-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Note Summaries](actions/list-note-summaries.md) | `GET /api/note-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Notebooks](actions/list-notebooks.md) | `GET /api/notebook` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Notes](actions/list-notes.md) | `GET /api/note` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Regarding](actions/list-regarding.md) | `GET /api/regarding` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Task Lists](actions/list-task-lists.md) | `GET /api/task-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Tasks](actions/list-tasks.md) | `GET /api/task-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List TE Comments](actions/list-te-comments.md) | `GET /api/te-comments` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Time Off Group Profiles](actions/list-time-off-group-profiles.md) | `GET /api/timeoff-group-profile` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Time Off Lists](actions/list-time-off-lists.md) | `GET /api/timeoff-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Time Offs](actions/list-time-offs.md) | `GET /api/timeoff-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Timesheet Details](actions/list-timesheet-details.md) | `GET /api/timesheet-detail` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Timesheet Group Profiles](actions/list-timesheet-group-profiles.md) | `GET /api/timesheet-group-profile` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Timesheet Lists](actions/list-timesheet-lists.md) | `GET /api/timesheet-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Timesheets](actions/list-timesheets.md) | `GET /api/timesheet-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Tracker Binders](actions/list-tracker-binders.md) | `GET /api/tracker-binder-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Tracker Cases](actions/list-tracker-cases.md) | `GET /api/tracker-case-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Tracker Lists](actions/list-tracker-lists.md) | `GET /api/tracker-lists` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Users](actions/list-users.md) | `GET /api/user-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [List Workflow Summaries](actions/list-workflow-summaries.md) | `GET /api/workflow-summary` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Account Detail](actions/update-account-detail.md) | `PUT /api/account-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Contact Detail](actions/update-contact-detail.md) | `PUT /api/contact-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Event Detail](actions/update-event-detail.md) | `PUT /api/event-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Expense](actions/update-expense.md) | `PUT /api/expense-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Expense Detail](actions/update-expense-detail.md) | `PUT /api/expense-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Note](actions/update-note.md) | `PUT /api/note/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Note Detail](actions/update-note-detail.md) | `PUT /api/note-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Notebook](actions/update-notebook.md) | `PUT /api/notebook/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Sub Task](actions/update-sub-task.md) | `PUT /api/subtask/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Task Detail](actions/update-task-detail.md) | `PUT /api/task-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Task Status](actions/update-task-status.md) | `PUT /api/task-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Time Off Detail](actions/update-time-off-detail.md) | `PUT /api/timeoff-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Timesheet](actions/update-timesheet.md) | `PUT /api/timesheet-summary/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Timesheet Detail](actions/update-timesheet-detail.md) | `PUT /api/timesheet-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
| [Update Tracker Case Detail](actions/update-tracker-case-detail.md) | `PUT /api/tracker-case-detail/{id}` | [docs](https://app.officeclip.com/swagger/ui/index) |
