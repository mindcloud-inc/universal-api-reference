# Cirra MCP Tests - Do Not Delete Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cirra MCP Tests - Do Not Delete expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-cursor?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cirra MCP Tests - Do Not Delete actions that support pagination

- [Pagination Cursor](actions/pagination-cursor.md)
- [Pagination Offset](actions/pagination-offset.md)
- [Pagination Page 1 Index](actions/pagination-page-one-index.md)
- [Pagination Page 0 Index](actions/pagination-page-zero-index.md)
