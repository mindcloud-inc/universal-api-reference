# LOBSTR.IO Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LOBSTR.IO expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-results?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LOBSTR.IO actions that support pagination

- [Get Results](actions/get-results.md)
- [List Accounts](actions/list-accounts.md)
- [List Crawlers](actions/list-crawlers.md)
- [List Runs](actions/list-runs.md)
- [List Squids](actions/list-squids.md)
- [List Tasks](actions/list-tasks.md)
