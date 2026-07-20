# Hightouch Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Hightouch expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-decision-engine-flows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Hightouch actions that support pagination

- [List Decision Engine Flows](actions/list-decision-engine-flows.md)
- [List Decision Engine Messages](actions/list-decision-engine-messages.md)
- [List Destinations](actions/list-destinations.md)
- [List Event Contracts](actions/list-event-contracts.md)
- [List IDR Runs](actions/list-idr-runs.md)
- [List Models](actions/list-models.md)
- [List Sources](actions/list-sources.md)
- [List Sync Runs](actions/list-sync-runs.md)
- [List Syncs](actions/list-syncs.md)
