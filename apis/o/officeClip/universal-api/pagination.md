# OfficeClip Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OfficeClip expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-account-children?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OfficeClip actions that support pagination

- [List Account Children](actions/list-account-children.md)
- [List Account Lists](actions/list-account-lists.md)
- [List Accounts](actions/list-accounts.md)
- [List Contact Children](actions/list-contact-children.md)
- [List Contact Lists](actions/list-contact-lists.md)
- [List Contacts](actions/list-contacts.md)
- [List Event Lists](actions/list-event-lists.md)
- [List Events](actions/list-events.md)
- [List Expense Details](actions/list-expense-details.md)
- [List Expense Group Profiles](actions/list-expense-group-profiles.md)
- [List Expense Lists](actions/list-expense-lists.md)
- [List Expenses](actions/list-expenses.md)
- [List Note Details](actions/list-note-details.md)
- [List Note Summaries](actions/list-note-summaries.md)
- [List Notebooks](actions/list-notebooks.md)
- [List Notes](actions/list-notes.md)
- [List Regarding](actions/list-regarding.md)
- [List Task Lists](actions/list-task-lists.md)
- [List Tasks](actions/list-tasks.md)
- [List TE Comments](actions/list-te-comments.md)
- [List Time Off Group Profiles](actions/list-time-off-group-profiles.md)
- [List Time Off Lists](actions/list-time-off-lists.md)
- [List Time Offs](actions/list-time-offs.md)
- [List Timesheet Details](actions/list-timesheet-details.md)
- [List Timesheet Group Profiles](actions/list-timesheet-group-profiles.md)
- [List Timesheet Lists](actions/list-timesheet-lists.md)
- [List Timesheets](actions/list-timesheets.md)
- [List Tracker Binders](actions/list-tracker-binders.md)
- [List Tracker Cases](actions/list-tracker-cases.md)
- [List Tracker Lists](actions/list-tracker-lists.md)
- [List Users](actions/list-users.md)
- [List Workflow Summaries](actions/list-workflow-summaries.md)
