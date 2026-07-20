# SE Ranking Data Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SE Ranking Data expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-keyword-rankings?connectionId=$CONNECTION_ID&limit=25&offset=0&source=us&domain=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SE Ranking Data actions that support pagination

- [Get Domain Keyword Rankings](actions/get-domain-keyword-rankings.md)
