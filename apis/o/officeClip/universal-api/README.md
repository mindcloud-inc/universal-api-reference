# <img src="https://images.mindcloud.co/apps/icons/office-clip_1775571641733.png" alt="OfficeClip logo" width="28" height="28"> OfficeClip: Universal API

Manage contacts, tasks, events, timesheets, expenses, and tracker cases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/officeClip/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 92
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.officeclip.com
- **Vendor API docs:** https://app.officeclip.com/swagger/ui/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (92)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Detail](actions/create-account-detail.md) | POST | Creates an account in OfficeClip. |
| [Delete Account Detail](actions/delete-account-detail.md) | DELETE | Deletes an account from OfficeClip. |
| [Get Account Detail](actions/get-account-detail.md) | GET | Retrieves an account from OfficeClip. |
| [List Account Children](actions/list-account-children.md) | GET | Retrieves account child lists from OfficeClip. |
| [List Account Lists](actions/list-account-lists.md) | GET | Retrieves account lists from OfficeClip. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from OfficeClip. |
| [Update Account Detail](actions/update-account-detail.md) | PUT | Updates an account in OfficeClip. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Detail](actions/create-contact-detail.md) | POST | Creates a contact in OfficeClip. |
| [Delete Contact Detail](actions/delete-contact-detail.md) | DELETE | Deletes a contact from OfficeClip. |
| [Get Contact Detail](actions/get-contact-detail.md) | GET | Retrieves a contact from OfficeClip. |
| [List Contact Children](actions/list-contact-children.md) | GET | Retrieves contact child lists from OfficeClip. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from OfficeClip. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from OfficeClip. |
| [Update Contact Detail](actions/update-contact-detail.md) | PUT | Updates a contact in OfficeClip. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Detail](actions/create-event-detail.md) | POST | Creates an event in OfficeClip. |
| [Delete Event Detail](actions/delete-event-detail.md) | DELETE | Deletes an event from OfficeClip. |
| [Get Event Detail](actions/get-event-detail.md) | GET | Retrieves an event from OfficeClip. |
| [List Event Lists](actions/list-event-lists.md) | GET | Retrieves event lists from OfficeClip. |
| [List Events](actions/list-events.md) | GET | Retrieves events from OfficeClip. |
| [Update Event Detail](actions/update-event-detail.md) | PUT | Updates an event in OfficeClip. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates an expense in OfficeClip. |
| [Create Expense Detail](actions/create-expense-detail.md) | POST | Creates an expense detail in OfficeClip. |
| [Delete Expense](actions/delete-expense.md) | DELETE | Deletes an expense from OfficeClip. |
| [Delete Expense Detail](actions/delete-expense-detail.md) | DELETE | Deletes an expense detail from OfficeClip. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from OfficeClip. |
| [Get Expense Detail](actions/get-expense-detail.md) | GET | Retrieves an expense detail from OfficeClip. |
| [List Expense Details](actions/list-expense-details.md) | GET | Retrieves expense details from OfficeClip. |
| [List Expense Group Profiles](actions/list-expense-group-profiles.md) | GET | Retrieves expense group profiles from OfficeClip. |
| [List Expense Lists](actions/list-expense-lists.md) | GET | Retrieves expense lists from OfficeClip. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from OfficeClip. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an expense in OfficeClip. |
| [Update Expense Detail](actions/update-expense-detail.md) | PUT | Updates an expense detail in OfficeClip. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image Detail](actions/create-image-detail.md) | POST | Creates an image detail in OfficeClip. |
| [Get Image Detail](actions/get-image-detail.md) | GET | Retrieves image details by image URL from OfficeClip. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a note in OfficeClip. |
| [Create Note Detail](actions/create-note-detail.md) | POST | Creates a note detail in OfficeClip. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes a note from OfficeClip. |
| [Delete Note Detail](actions/delete-note-detail.md) | DELETE | Deletes a note detail from OfficeClip. |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from OfficeClip. |
| [Get Note Detail](actions/get-note-detail.md) | GET | Retrieves a note detail from OfficeClip. |
| [List Note Details](actions/list-note-details.md) | GET | Retrieves note details from OfficeClip. |
| [List Note Summaries](actions/list-note-summaries.md) | GET | Retrieves note summaries from OfficeClip. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from OfficeClip. |
| [Update Note](actions/update-note.md) | PUT | Updates a note in OfficeClip. |
| [Update Note Detail](actions/update-note-detail.md) | PUT | Updates a note detail in OfficeClip. |

### Notebook

| Action | Method | Description |
| --- | --- | --- |
| [Create Notebook](actions/create-notebook.md) | POST | Creates a notebook in OfficeClip. |
| [Delete Notebook](actions/delete-notebook.md) | DELETE | Deletes a notebook from OfficeClip. |
| [List Notebooks](actions/list-notebooks.md) | GET | Retrieves notebooks from OfficeClip. |
| [Update Notebook](actions/update-notebook.md) | PUT | Updates a notebook in OfficeClip. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Lists](actions/get-profile-lists.md) | GET | Retrieves profile lists from OfficeClip. |

### Regarding

| Action | Method | Description |
| --- | --- | --- |
| [List Regarding](actions/list-regarding.md) | GET | Retrieves regarding lists from OfficeClip. |

### Sub Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Sub Task](actions/create-sub-task.md) | POST | Creates a subtask in OfficeClip. |
| [Delete Sub Task](actions/delete-sub-task.md) | DELETE | Deletes a subtask from OfficeClip. |
| [Update Sub Task](actions/update-sub-task.md) | PUT | Updates a subtask in OfficeClip. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Detail](actions/create-task-detail.md) | POST | Creates a task detail in OfficeClip. |
| [Delete Task Detail](actions/delete-task-detail.md) | DELETE | Deletes a task detail from OfficeClip. |
| [Get Task Detail](actions/get-task-detail.md) | GET | Retrieves a task detail from OfficeClip. |
| [Get Task Detail by Query ID](actions/get-task-detail-by-query-id.md) | GET | Retrieves task details by query ID from OfficeClip. |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from OfficeClip. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from OfficeClip. |
| [Update Task Detail](actions/update-task-detail.md) | PUT | Updates a task detail in OfficeClip. |
| [Update Task Status](actions/update-task-status.md) | PUT | Updates a task's completion status in OfficeClip. |

### Te Comment

| Action | Method | Description |
| --- | --- | --- |
| [List TE Comments](actions/list-te-comments.md) | GET | Retrieves timesheet and expense comments from OfficeClip. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Off Detail](actions/create-time-off-detail.md) | POST | Creates a time off entry in OfficeClip. |
| [Delete Time Off Detail](actions/delete-time-off-detail.md) | DELETE | Deletes a time off entry from OfficeClip. |
| [Get Time Off Detail](actions/get-time-off-detail.md) | GET | Retrieves a time off entry from OfficeClip. |
| [List Time Off Group Profiles](actions/list-time-off-group-profiles.md) | GET | Retrieves time off group profiles from OfficeClip. |
| [List Time Off Lists](actions/list-time-off-lists.md) | GET | Retrieves time off lists from OfficeClip. |
| [List Time Offs](actions/list-time-offs.md) | GET | Retrieves time off entries from OfficeClip. |
| [Update Time Off Detail](actions/update-time-off-detail.md) | PUT | Updates a time off entry in OfficeClip. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST | Creates a timesheet in OfficeClip. |
| [Create Timesheet Detail](actions/create-timesheet-detail.md) | POST | Creates a timesheet detail in OfficeClip. |
| [Delete Timesheet](actions/delete-timesheet.md) | DELETE | Deletes a timesheet from OfficeClip. |
| [Delete Timesheet Detail](actions/delete-timesheet-detail.md) | DELETE | Deletes a timesheet detail from OfficeClip. |
| [Get Timesheet](actions/get-timesheet.md) | GET | Retrieves a timesheet from OfficeClip. |
| [Get Timesheet Detail](actions/get-timesheet-detail.md) | GET | Retrieves a timesheet detail from OfficeClip. |
| [List Timesheet Details](actions/list-timesheet-details.md) | GET | Retrieves timesheet details from OfficeClip. |
| [List Timesheet Group Profiles](actions/list-timesheet-group-profiles.md) | GET | Retrieves timesheet group profiles from OfficeClip. |
| [List Timesheet Lists](actions/list-timesheet-lists.md) | GET | Retrieves timesheet lists from OfficeClip. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from OfficeClip. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates a timesheet in OfficeClip. |
| [Update Timesheet Detail](actions/update-timesheet-detail.md) | PUT | Updates a timesheet detail in OfficeClip. |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [List Tracker Lists](actions/list-tracker-lists.md) | GET | Retrieves tracker lists from OfficeClip. |

### Tracker Binder

| Action | Method | Description |
| --- | --- | --- |
| [List Tracker Binders](actions/list-tracker-binders.md) | GET | Retrieves tracker binders from OfficeClip. |

### Tracker Case

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracker Case Detail](actions/create-tracker-case-detail.md) | POST | Creates a tracker case detail in OfficeClip. |
| [Delete Tracker Case Detail](actions/delete-tracker-case-detail.md) | DELETE | Deletes a tracker case detail from OfficeClip. |
| [Get Tracker Case Detail](actions/get-tracker-case-detail.md) | GET | Retrieves a tracker case detail from OfficeClip. |
| [List Tracker Cases](actions/list-tracker-cases.md) | GET | Retrieves tracker cases from OfficeClip. |
| [Update Tracker Case Detail](actions/update-tracker-case-detail.md) | PUT | Updates a tracker case detail in OfficeClip. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from OfficeClip. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Summary](actions/create-workflow-summary.md) | POST | Creates a workflow summary in OfficeClip. |
| [List Workflow Summaries](actions/list-workflow-summaries.md) | GET | Retrieves workflow summaries from OfficeClip. |

