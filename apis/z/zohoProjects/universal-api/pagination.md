# Zoho Projects Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho Projects expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portal-users-client-users-and-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&portalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho Projects actions that support pagination

- [List Portal Users, Client Users, And Contacts](actions/list-portal-users-client-users-and-contacts.md)
- [List Project Issues](actions/list-project-issues.md)
- [List Tasks By Project](actions/list-tasks-by-project.md)
