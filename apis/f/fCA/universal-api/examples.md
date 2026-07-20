# FCA Universal API Examples

These examples use the MindCloud API key and FCA connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List regulated markets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fCA/latest/actions/list-regulated-markets?${params}`, {
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

See the full [List regulated markets action reference](actions/list-regulated-markets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fCA/latest/actions/list-regulated-markets).
