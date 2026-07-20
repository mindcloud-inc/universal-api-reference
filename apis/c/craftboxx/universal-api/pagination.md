# Craftboxx Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Craftboxx expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Craftboxx actions that support pagination

- [List Articles](actions/list-articles.md)
- [List Assignments](actions/list-assignments.md)
- [List Customers](actions/list-customers.md)
- [List Employees](actions/list-employees.md)
- [List Projects](actions/list-projects.md)
- [List Timesheets](actions/list-timesheets.md)
