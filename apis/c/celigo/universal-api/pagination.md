# Celigo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Celigo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Celigo actions that support pagination

- [List Audit Logs](actions/list-audit-logs.md)
- [List Connections](actions/list-connections.md)
- [List Exports](actions/list-exports.md)
- [List Flows](actions/list-flows.md)
- [List Imports](actions/list-imports.md)
- [List Integrations](actions/list-integrations.md)
