# Productive.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Productive.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Productive.io actions that support pagination

- [List Bookings](actions/list-bookings.md)
- [List Companies](actions/list-companies.md)
- [List Contact Entries](actions/list-contact-entries.md)
- [List Contracts](actions/list-contracts.md)
- [List Deals](actions/list-deals.md)
- [List Expenses](actions/list-expenses.md)
- [List Invoices](actions/list-invoices.md)
- [List Organizations](actions/list-organizations.md)
- [List People](actions/list-people.md)
- [List Project Assignments](actions/list-project-assignments.md)
- [List Projects](actions/list-projects.md)
- [List Task Lists](actions/list-task-lists.md)
- [List Tasks](actions/list-tasks.md)
- [List Teams](actions/list-teams.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Timers](actions/list-timers.md)
- [List Timesheets](actions/list-timesheets.md)
- [List Users](actions/list-users.md)
- [List Workflow Statuses](actions/list-workflow-statuses.md)
- [List Workflows](actions/list-workflows.md)
