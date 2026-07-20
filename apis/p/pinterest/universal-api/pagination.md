# Pinterest Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pinterest expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-ad-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pinterest actions that support pagination

- [List Ad Accounts](actions/list-ad-accounts.md)
- [List Ad Groups](actions/list-ad-groups.md)
- [List Ads](actions/list-ads.md)
- [List Board Pins](actions/list-board-pins.md)
- [List Board Section Pins](actions/list-board-section-pins.md)
- [List Board Sections](actions/list-board-sections.md)
- [List Boards](actions/list-boards.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Catalogs](actions/list-catalogs.md)
- [List Followers](actions/list-followers.md)
- [List Pins](actions/list-pins.md)
- [List Product Groups](actions/list-product-groups.md)
- [List Products By Product Group](actions/list-products-by-product-group.md)
- [Search Boards](actions/search-boards.md)
