# Google Search Console Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Google Search Console expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/query-search-analytics?connectionId=$CONNECTION_ID&limit=25&offset=0&siteUrl=https%3A%2F%2Fexample.com&startDate=YYYY-MM-DD&endDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Google Search Console actions that support pagination

- [Query Search Analytics](actions/query-search-analytics.md)
