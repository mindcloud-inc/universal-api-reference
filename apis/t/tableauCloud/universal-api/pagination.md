# Tableau Cloud Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Tableau Cloud expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-flow-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Tableau Cloud actions that support pagination

- [Get Flow Runs](actions/get-flow-runs.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [Query Data Sources](actions/query-data-sources.md)
- [Query Flows for User](actions/query-flows-for-user.md)
- [Query Projects](actions/query-projects.md)
- [Query Views for Site](actions/query-views-for-site.md)
- [Query Workbooks for Site](actions/query-workbooks-for-site.md)
- [Query Workbooks for User](actions/query-workbooks-for-user.md)
