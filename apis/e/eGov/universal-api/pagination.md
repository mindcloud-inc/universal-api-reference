# e-Gov Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model e-Gov expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-dataset-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&id=moj_20180907_0008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## e-Gov actions that support pagination

- [List Dataset Activity](actions/list-dataset-activity.md)
- [List Datasets With Resources](actions/list-datasets-with-resources.md)
- [List Group Activity](actions/list-group-activity.md)
- [List Groups](actions/list-groups.md)
- [List Organization Activity](actions/list-organization-activity.md)
- [List Organizations](actions/list-organizations.md)
- [List Recently Changed Dataset Activity](actions/list-recently-changed-dataset-activity.md)
- [List User Activity](actions/list-user-activity.md)
- [Search Tags](actions/search-tags.md)
