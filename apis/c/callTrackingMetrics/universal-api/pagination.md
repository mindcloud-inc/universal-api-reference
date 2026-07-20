# CallTrackingMetrics Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CallTrackingMetrics expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-agent-events?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=string&startTime=1&endTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CallTrackingMetrics actions that support pagination

- [Get Agent Events](actions/get-agent-events.md)
- [List Activities](actions/list-activities.md)
- [List Call Setting Number Assignments](actions/list-call-setting-number-assignments.md)
- [List Call Settings](actions/list-call-settings.md)
- [List Tracking Sources](actions/list-tracking-sources.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
- [Lookup Objects](actions/lookup-objects.md)
