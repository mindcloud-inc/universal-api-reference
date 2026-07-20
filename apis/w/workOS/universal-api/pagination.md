# WorkOS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WorkOS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WorkOS actions that support pagination

- [List Connections](actions/list-connections.md)
- [List Directories](actions/list-directories.md)
- [List Directory Groups](actions/list-directory-groups.md)
- [List Directory Users](actions/list-directory-users.md)
- [List events](actions/list-events.md)
- [List feature flags](actions/list-feature-flags.md)
- [List invitations](actions/list-invitations.md)
- [List organization memberships](actions/list-organization-memberships.md)
- [List Organizations](actions/list-organizations.md)
- [List permissions](actions/list-permissions.md)
- [List role assignments](actions/list-role-assignments.md)
- [List sessions](actions/list-sessions.md)
- [List users](actions/list-users.md)
- [List Webhook Endpoints](actions/list-webhook-endpoints.md)
