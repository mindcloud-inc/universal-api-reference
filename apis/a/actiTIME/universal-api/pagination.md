# actiTIME Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model actiTIME expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-customer-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## actiTIME actions that support pagination

- [List Customer Comments](actions/list-customer-comments.md)
- [List Customers](actions/list-customers.md)
- [List Departments](actions/list-departments.md)
- [List Leave Types](actions/list-leave-types.md)
- [List Project Comments](actions/list-project-comments.md)
- [List Projects](actions/list-projects.md)
- [List Task Comments](actions/list-task-comments.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Zone Groups](actions/list-time-zone-groups.md)
- [List Types of Work](actions/list-types-of-work.md)
- [List Users](actions/list-users.md)
- [List Workflow Statuses](actions/list-workflow-statuses.md)
