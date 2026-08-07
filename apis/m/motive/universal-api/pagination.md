# Motive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Motive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Motive actions that support pagination

- [List assets](actions/list-assets.md)
- [List driver performance events](actions/list-driver-performance-events.md)
- [List driver utilization](actions/list-driver-utilization.md)
- [List scorecard summaries](actions/list-scorecard-summaries.md)
- [List users](actions/list-users.md)
- [List vehicle utilization](actions/list-vehicle-utilization.md)
- [List vehicles](actions/list-vehicles.md)
