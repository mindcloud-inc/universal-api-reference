# Microsoft Entra Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Microsoft Entra expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-group-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Microsoft Entra actions that support pagination

- [List Group Memberships](actions/list-group-memberships.md)
- [List Group Transitive Memberships](actions/list-group-transitive-memberships.md)
- [List Groups](actions/list-groups.md)
- [List User Direct Reports](actions/list-user-direct-reports.md)
- [List User Memberships](actions/list-user-memberships.md)
- [List User Owned Objects](actions/list-user-owned-objects.md)
- [List User Transitive Memberships](actions/list-user-transitive-memberships.md)
- [List Users](actions/list-users.md)
