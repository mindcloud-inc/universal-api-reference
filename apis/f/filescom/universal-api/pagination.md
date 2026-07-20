# Files.com Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Files.com expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-automations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Files.com actions that support pagination

- [List Automations](actions/list-automations.md)
- [List Bundles](actions/list-bundles.md)
- [List File History](actions/list-file-history.md)
- [List Folder Contents](actions/list-folder-contents.md)
- [List Folder History](actions/list-folder-history.md)
- [List Groups](actions/list-groups.md)
- [List History](actions/list-history.md)
- [List Login History](actions/list-login-history.md)
- [List Notifications](actions/list-notifications.md)
- [List Permissions](actions/list-permissions.md)
- [List Projects](actions/list-projects.md)
- [List Requests](actions/list-requests.md)
- [List Requests by Folder Path](actions/list-requests-by-folder-path.md)
- [List Syncs](actions/list-syncs.md)
- [List User History](actions/list-user-history.md)
- [List Users](actions/list-users.md)
- [List Workspaces](actions/list-workspaces.md)
