# Better Stack Telemetry Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Better Stack Telemetry expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Better Stack Telemetry actions that support pagination

- [List Metrics](actions/list-metrics.md)
- [List Source Groups](actions/list-source-groups.md)
- [List Sources](actions/list-sources.md)
- [List Sources In Source Group](actions/list-sources-in-source-group.md)
