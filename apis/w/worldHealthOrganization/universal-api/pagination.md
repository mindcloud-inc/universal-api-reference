# World Health Organization Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model World Health Organization expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-age-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## World Health Organization actions that support pagination

- [List Age Groups](actions/list-age-groups.md)
- [List Countries](actions/list-countries.md)
- [List Dimension Values](actions/list-dimension-values.md)
- [List Dimensions](actions/list-dimensions.md)
- [List Income Groups](actions/list-income-groups.md)
- [List Indicator Data](actions/list-indicator-data.md)
- [List Indicator Dimensions](actions/list-indicator-dimensions.md)
- [List Indicators](actions/list-indicators.md)
- [List Publish States](actions/list-publish-states.md)
- [List Region Countries](actions/list-region-countries.md)
- [List Sex Values](actions/list-sex-values.md)
- [List WHO Regions](actions/list-who-regions.md)
- [List Year Values](actions/list-year-values.md)
