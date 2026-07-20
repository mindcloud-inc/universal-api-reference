# Layer4 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Layer4 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-record-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Layer4 actions that support pagination

- [List Record Requests](actions/list-record-requests.md)
- [List Records](actions/list-records.md)
- [List Token Requests](actions/list-token-requests.md)
- [List Tokens](actions/list-tokens.md)
- [List Wallets](actions/list-wallets.md)
