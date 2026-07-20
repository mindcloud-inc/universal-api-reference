# IronWiFi Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model IronWiFi expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-access-points?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## IronWiFi actions that support pagination

- [List Access Points](actions/list-access-points.md)
- [List Captive Portals](actions/list-captive-portals.md)
- [List Configurations](actions/list-configurations.md)
- [List Connectors](actions/list-connectors.md)
- [List Devices](actions/list-devices.md)
- [List Employees](actions/list-employees.md)
- [List Fleets](actions/list-fleets.md)
- [List Groups](actions/list-groups.md)
- [List Guest Profiles](actions/list-guest-profiles.md)
- [List Guests](actions/list-guests.md)
- [List Networks](actions/list-networks.md)
- [List Org Unit Group Mappings](actions/list-org-unit-group-mappings.md)
- [List Organization Units](actions/list-organization-units.md)
- [List Shared Files](actions/list-shared-files.md)
- [List Tariff Groups](actions/list-tariff-groups.md)
- [List Tariffs](actions/list-tariffs.md)
- [List Themes](actions/list-themes.md)
- [List Translations](actions/list-translations.md)
- [List Users](actions/list-users.md)
- [List Variables](actions/list-variables.md)
- [List Vehicles](actions/list-vehicles.md)
- [List Venues](actions/list-venues.md)
- [List Vouchers](actions/list-vouchers.md)
