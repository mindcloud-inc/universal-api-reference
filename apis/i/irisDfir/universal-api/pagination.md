# Iris Dfir Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Iris Dfir expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Iris Dfir actions that support pagination

- [List Alerts](actions/list-alerts.md)
- [List Alerts Legacy](actions/list-alerts-legacy.md)
- [List Assets](actions/list-assets.md)
- [List Cases](actions/list-cases.md)
- [List Note Directories](actions/list-note-directories.md)
- [List Tasks](actions/list-tasks.md)
