# Statistics Netherlands CBS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Statistics Netherlands CBS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-featured-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Statistics Netherlands CBS actions that support pagination

- [List Featured Groups](actions/list-featured-groups.md)
- [List Feed Category Groups](actions/list-feed-category-groups.md)
- [List Feed Data Properties](actions/list-feed-data-properties.md)
- [List Feed Resource Rows](actions/list-feed-resource-rows.md)
- [List Feed Table Infos](actions/list-feed-table-infos.md)
- [List Feed Typed Data Rows](actions/list-feed-typed-data-rows.md)
- [List Feed Untyped Data Rows](actions/list-feed-untyped-data-rows.md)
- [List OData V4 Datasets](actions/list-o-data-v4-datasets.md)
- [List Table Featured Links](actions/list-table-featured-links.md)
- [List Table Theme Links](actions/list-table-theme-links.md)
- [List Tables](actions/list-tables.md)
- [List Themes](actions/list-themes.md)
