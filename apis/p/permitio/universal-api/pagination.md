# Permit.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Permit.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&projId=string&envId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Permit.io actions that support pagination

- [List Audit Logs](actions/list-audit-logs.md)
- [List Environments](actions/list-environments.md)
- [List Organizations](actions/list-organizations.md)
- [List Projects](actions/list-projects.md)
- [List Resources](actions/list-resources.md)
- [List Role Assignments](actions/list-role-assignments.md)
- [List Roles](actions/list-roles.md)
- [List Tenants](actions/list-tenants.md)
- [List Users](actions/list-users.md)
