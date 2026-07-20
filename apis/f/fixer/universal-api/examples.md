# Fixer Universal API Examples

These examples use the MindCloud API key and Fixer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Symbols

Retrieves supported currency symbols from Fixer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols?${params}`, {
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
  "data": [
    {
      "code": "string",
      "description": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Symbols action reference](actions/list-supported-symbols.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fixer/latest/actions/list-supported-symbols).
