# Launch Library 2 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Launch Library 2 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Launch Library 2 actions that support pagination

- [List Agencies](actions/list-agencies.md)
- [List Astronauts](actions/list-astronauts.md)
- [List Docking Events](actions/list-docking-events.md)
- [List Events](actions/list-events.md)
- [List Expeditions](actions/list-expeditions.md)
- [List Launcher Configurations](actions/list-launcher-configurations.md)
- [List Launches](actions/list-launches.md)
- [List Locations](actions/list-locations.md)
- [List Pads](actions/list-pads.md)
- [List Payloads](actions/list-payloads.md)
- [List Previous Events](actions/list-previous-events.md)
- [List Previous Launches](actions/list-previous-launches.md)
- [List Programs](actions/list-programs.md)
- [List Space Stations](actions/list-space-stations.md)
- [List Spacecraft](actions/list-spacecraft.md)
- [List Spacewalks](actions/list-spacewalks.md)
- [List Upcoming Events](actions/list-upcoming-events.md)
- [List Upcoming Launches](actions/list-upcoming-launches.md)
- [List Updates](actions/list-updates.md)
