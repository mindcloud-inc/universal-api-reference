# Seam Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Seam expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-connect-webviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Seam actions that support pagination

- [List Connect Webviews](actions/list-connect-webviews.md)
- [List Connected Accounts](actions/list-connected-accounts.md)
- [List Devices](actions/list-devices.md)
- [List Locks](actions/list-locks.md)
- [List Noise Sensors](actions/list-noise-sensors.md)
- [List Thermostats](actions/list-thermostats.md)
