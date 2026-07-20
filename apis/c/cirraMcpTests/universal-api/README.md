# Cirra MCP Tests - Do Not Delete: Universal API

Cirra MCP Tests - Do Not Delete through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cirraMcpTests/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Pagination Cursor](actions/pagination-cursor.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-cursor?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Pagination Cursor](actions/pagination-cursor.md) | GET |  |
| [Pagination Offset](actions/pagination-offset.md) | GET |  |
| [Pagination Page 1 Index](actions/pagination-page-one-index.md) | GET |  |
| [Pagination Page 0 Index](actions/pagination-page-zero-index.md) | GET |  |

