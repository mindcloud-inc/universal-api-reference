# Federal Reserve Economic Data Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Federal Reserve Economic Data expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-category-series?connectionId=$CONNECTION_ID&limit=25&offset=0&category_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Federal Reserve Economic Data actions that support pagination

- [List Category Series](actions/list-category-series.md)
- [List Category Tags](actions/list-category-tags.md)
- [List Release Dates](actions/list-release-dates.md)
- [List Release Dates For Release](actions/list-release-dates-for-release.md)
- [List Release Series](actions/list-release-series.md)
- [List Releases](actions/list-releases.md)
- [List Series Observations](actions/list-series-observations.md)
- [List Series Updates](actions/list-series-updates.md)
- [List Source Releases](actions/list-source-releases.md)
- [List Sources](actions/list-sources.md)
- [Search Series](actions/search-series.md)
