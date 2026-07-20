# SerpApi Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SerpApi expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-duckduckgo-light?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SerpApi actions that support pagination

- [Search DuckDuckGo Light](actions/search-duckduckgo-light.md)
- [Search DuckDuckGo Web](actions/search-duckduckgo-web.md)
- [Search Google](actions/search-google.md)
- [Search Google Events](actions/search-google-events.md)
- [Search Google Finance](actions/search-google-finance.md)
- [Search Google Forums](actions/search-google-forums.md)
- [Search Google Images](actions/search-google-images.md)
- [Search Google Jobs](actions/search-google-jobs.md)
- [Search Google Light](actions/search-google-light.md)
- [Search Google Local](actions/search-google-local.md)
- [Search Google Maps](actions/search-google-maps.md)
- [Search Google News](actions/search-google-news.md)
- [Search Google Patents](actions/search-google-patents.md)
- [Search Google Scholar](actions/search-google-scholar.md)
- [Search Google Shopping](actions/search-google-shopping.md)
- [Search Google Trends](actions/search-google-trends.md)
- [Search Google Videos](actions/search-google-videos.md)
