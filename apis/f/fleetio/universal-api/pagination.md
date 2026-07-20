# Fleetio Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Fleetio expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Fleetio actions that support pagination

- [List Contacts](actions/list-contacts.md)
- [List Fuel Entries](actions/list-fuel-entries.md)
- [List Issues](actions/list-issues.md)
- [List Meter Entries](actions/list-meter-entries.md)
- [List Service Entries](actions/list-service-entries.md)
- [List Vehicles](actions/list-vehicles.md)
- [List Vendors](actions/list-vendors.md)
- [List Work Orders](actions/list-work-orders.md)
