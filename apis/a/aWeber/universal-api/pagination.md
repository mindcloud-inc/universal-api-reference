# AWeber Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model AWeber expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/find-lists?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## AWeber actions that support pagination

- [Find Lists](actions/find-lists.md)
- [Find Subscribers For Account](actions/find-subscribers-for-account.md)
- [Find Subscribers For List](actions/find-subscribers-for-list.md)
- [List Accounts](actions/list-accounts.md)
- [List Broadcasts](actions/list-broadcasts.md)
- [List Integrations](actions/list-integrations.md)
- [List Lists](actions/list-lists.md)
- [List Subscribers](actions/list-subscribers.md)
