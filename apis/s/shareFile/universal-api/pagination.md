# ShareFile Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ShareFile expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-current-account?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ShareFile actions that support pagination

- [Get Current Account](actions/get-current-account.md)
- [Get Current User](actions/get-current-user.md)
- [Get Home Folder for Current User](actions/get-home-folder-for-current-user.md)
- [List Groups](actions/list-groups.md)
- [List Item Children](actions/list-item-children.md)
- [List Shares](actions/list-shares.md)
- [List Zones](actions/list-zones.md)
