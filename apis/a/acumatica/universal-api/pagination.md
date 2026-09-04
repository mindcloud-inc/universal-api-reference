# Acumatica Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Acumatica expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&wse=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Acumatica actions that support pagination

- [List Projects](actions/list-projects.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [Search By Entity](actions/search-by-entity.md)
- [Search By Generic Inquiry](actions/search-by-generic-inquiry.md)
