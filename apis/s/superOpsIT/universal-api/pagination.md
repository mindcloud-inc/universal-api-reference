# SuperOps IT Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SuperOps IT expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-asset-software?connectionId=$CONNECTION_ID&limit=25&offset=0&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SuperOps IT actions that support pagination

- [List Asset Software](actions/list-asset-software.md)
- [List Assets](actions/list-assets.md)
- [List Sites](actions/list-sites.md)
- [List Tasks](actions/list-tasks.md)
- [List Tickets](actions/list-tickets.md)
- [List Users](actions/list-users.md)
