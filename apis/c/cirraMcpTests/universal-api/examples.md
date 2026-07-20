# Cirra MCP Tests - Do Not Delete Universal API Examples

These examples use the MindCloud API key and Cirra MCP Tests - Do Not Delete connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Pagination Cursor



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-cursor?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-cursor?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Pagination Cursor action reference](actions/pagination-cursor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cirraMcpTests/latest/actions/pagination-cursor).
