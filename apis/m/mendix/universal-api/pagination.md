# Mendix Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mendix expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-project-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mendix actions that support pagination

- [List Account Project Roles](actions/list-account-project-roles.md)
- [List Account Projects](actions/list-account-projects.md)
- [List Project Members](actions/list-project-members.md)
- [List Projects](actions/list-projects.md)
- [List User Projects](actions/list-user-projects.md)
