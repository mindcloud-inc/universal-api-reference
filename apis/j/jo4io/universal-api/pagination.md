# jo4.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model jo4.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-conversions?connectionId=$CONNECTION_ID&limit=25&offset=0&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## jo4.io actions that support pagination

- [List Conversions](actions/get-conversions.md)
- [List My Teams](actions/get-my-teams.md)
- [List My URLs](actions/get-my-urls.md)
