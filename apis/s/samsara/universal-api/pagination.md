# Samsara Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Samsara expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-hos-clocks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Samsara actions that support pagination

- [Create Driver](actions/create-driver.md)
- [Get HOS Clocks](actions/get-hos-clocks.md)
- [Get Vehicle Locations](actions/get-vehicle-locations.md)
- [Get Vehicle Stats](actions/get-vehicle-stats.md)
- [List Addresses](actions/list-addresses.md)
- [List Drivers](actions/list-all-drivers.md)
- [List Tags](actions/list-all-tags1.md)
- [List Vehicles](actions/list-all-vehicles.md)
- [List Assets](actions/list-assets.md)
- [List Driver-Vehicle Assignments](actions/list-driver-vehicle-assignments.md)
- [List Equipment](actions/list-equipment.md)
- [List Routes](actions/list-routes.md)
- [List Trailers](actions/list-trailers.md)
- [List User Roles](actions/list-user-roles.md)
- [List Users](actions/list-users.md)
- [Stream DVIR Defects](actions/stream-dvir-defects.md)
- [Stream DVIRs](actions/stream-dvirs.md)
- [Update Driver](actions/update-driver.md)
