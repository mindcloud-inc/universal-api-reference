# Cirra Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cirra expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/get-user-apps?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cirra actions that support pagination

- [Get User Apps](actions/get-user-apps.md)
- [List Members](actions/list-members.md)
- [List Role App Permissions](actions/list-role-app-permissions.md)
- [List Role Model Permissions](actions/list-role-model-permissions.md)
- [List Roles](actions/list-roles.md)
- [List Threads](actions/list-threads.md)
