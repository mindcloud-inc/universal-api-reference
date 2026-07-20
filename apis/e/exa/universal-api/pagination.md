# Exa Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Exa expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Exa actions that support pagination

- [List Events](actions/list-events.md)
- [List Imports](actions/list-imports.md)
- [List Monitor Runs](actions/list-monitor-runs.md)
- [List Monitors](actions/list-monitors.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Webset Items](actions/list-webset-items.md)
- [List Websets](actions/list-websets.md)
