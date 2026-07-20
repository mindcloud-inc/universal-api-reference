# NewsData.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NewsData.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-archived-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NewsData.io actions that support pagination

- [List Archived News](actions/list-archived-news.md)
- [List Crypto News](actions/list-crypto-news.md)
- [List Latest News](actions/list-latest-news.md)
- [List Market News](actions/list-market-news.md)
