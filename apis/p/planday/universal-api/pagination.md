# Planday Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Planday expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-absence-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Planday actions that support pagination

- [List Absence Requests](actions/list-absence-requests.md)
- [List Deactivated Employees](actions/list-deactivated-employees.md)
- [List Departments](actions/list-departments.md)
- [List Employees](actions/list-employees.md)
- [List Positions](actions/list-positions.md)
- [List Punch Clock Records](actions/list-punch-clock-records.md)
- [List Shift Types](actions/list-shift-types.md)
- [List Shifts](actions/list-shifts.md)
