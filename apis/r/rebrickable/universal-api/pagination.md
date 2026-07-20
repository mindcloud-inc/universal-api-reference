# Rebrickable Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rebrickable expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-alternate-builds-for-set?connectionId=$CONNECTION_ID&limit=25&offset=0&setNum=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rebrickable actions that support pagination

- [List Alternate Builds for Set](actions/list-alternate-builds-for-set.md)
- [List Badges](actions/list-badges.md)
- [List Colors](actions/list-colors.md)
- [List Minifig Parts](actions/list-minifig-parts.md)
- [List Minifigs](actions/list-minifigs.md)
- [List Part Categories](actions/list-part-categories.md)
- [List Part Colors](actions/list-part-colors.md)
- [List Parts](actions/list-parts.md)
- [List Set Minifigs](actions/list-set-minifigs.md)
- [List Set Parts](actions/list-set-parts.md)
- [List Set Subsets](actions/list-set-subsets.md)
- [List Sets](actions/list-sets.md)
- [List Sets Containing Minifig](actions/list-sets-containing-minifig.md)
- [List Sets Containing Part Color](actions/list-sets-containing-part-color.md)
- [List Themes](actions/list-themes.md)
