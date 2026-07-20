# Nightfall.ai Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Nightfall.ai expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-event-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Nightfall.ai actions that support pagination

- [Get Exfiltration Event Activity](actions/get-exfiltration-event-activity.md)
- [Get Posture Event Activity](actions/get-posture-event-activity.md)
- [Get Violation Activity](actions/get-violation-activity.md)
- [Get Violation Findings](actions/get-violation-findings.md)
- [List Endpoint Devices](actions/list-endpoint-devices.md)
- [List Exfiltration Events](actions/list-exfiltration-events.md)
- [List GitHub Repositories](actions/list-git-hub-repositories.md)
- [List Posture Events](actions/list-posture-events.md)
- [List Violations](actions/list-violations.md)
- [Search Exfiltration Events](actions/search-exfiltration-events.md)
- [Search Posture Events](actions/search-posture-events.md)
- [Search Violations](actions/search-violations.md)
