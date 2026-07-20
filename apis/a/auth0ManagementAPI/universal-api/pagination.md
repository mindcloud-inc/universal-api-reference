# Auth0 Management Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Auth0 Management expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Auth0 Management actions that support pagination

- [List Clients](actions/list-clients.md)
- [List Organization Connections](actions/list-organization-connections.md)
- [List Organization Members](actions/list-organization-members.md)
- [List Organizations](actions/list-organizations.md)
- [List Role Permissions](actions/list-role-permissions.md)
- [List Role Users](actions/list-role-users.md)
- [List Roles](actions/list-roles.md)
- [List User Roles](actions/list-user-roles.md)
- [List Users](actions/list-users.md)
