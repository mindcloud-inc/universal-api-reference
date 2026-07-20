# bitFit Asset Management Software Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model bitFit Asset Management Software expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## bitFit Asset Management Software actions that support pagination

- [List Assets](actions/list-assets.md)
- [List Attachments](actions/list-attachments.md)
- [List Companies](actions/list-companies.md)
- [List Configs](actions/list-configs.md)
- [List Consumables](actions/list-consumables.md)
- [List Groups](actions/list-groups.md)
- [List Inventory Rules](actions/list-inventory-rules.md)
- [List Lists](actions/list-lists.md)
- [List Locations](actions/list-locations.md)
- [List Pages](actions/list-pages.md)
- [List Requests](actions/list-requests.md)
- [List Roles](actions/list-roles.md)
- [List Users](actions/list-users.md)
- [List Widget Configs](actions/list-widget-configs.md)
- [List Widgets](actions/list-widgets.md)
