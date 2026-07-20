# Dotdigital Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Dotdigital expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-campaigns-with-filters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Dotdigital actions that support pagination

- [Get All Campaigns With Filters](actions/get-all-campaigns-with-filters.md)
- [Get Forms](actions/get-forms.md)
- [Get Lists](actions/get-lists.md)
- [Get Private Lists](actions/get-private-lists.md)
- [Get Programs](actions/get-programs.md)
- [Get Public Lists](actions/get-public-lists.md)
- [Get Templates](actions/get-templates.md)
