# Ubidots Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Ubidots expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-dashboards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Ubidots actions that support pagination

- [Get all Dashboards](actions/get-all-dashboards.md)
- [Get all Device Groups](actions/get-all-device-groups.md)
- [Get all Device Types](actions/get-all-device-types.md)
- [Get all Devices](actions/get-all-devices.md)
- [Get all Events](actions/get-all-events.md)
- [Get all Organizations](actions/get-all-organizations.md)
- [Get all Users](actions/get-all-users.md)
- [Get all Variables](actions/get-all-variables.md)
- [Get Device Variables](actions/get-device-variables.md)
- [Get Event Logs](actions/get-event-logs.md)
- [Get Organization Devices](actions/get-organization-devices.md)
