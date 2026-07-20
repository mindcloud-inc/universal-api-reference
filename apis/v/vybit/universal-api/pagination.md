# Vybit Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Vybit expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-peeps?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Vybit actions that support pagination

- [List All Peeps](actions/list-all-peeps.md)
- [List Logs for Owned Vybit](actions/list-logs-for-owned-vybit.md)
- [List Logs for Subscription Following](actions/list-logs-for-subscription-following.md)
- [List Peeps for Vybit](actions/list-peeps-for-vybit.md)
