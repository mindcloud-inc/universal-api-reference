# Implisense Universal API Examples

These examples use the MindCloud API key and Implisense connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Companies

Finds companies in Implisense API by known attributes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies?${params}`, {
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
      "active": true,
      "city": "string",
      "id": "string",
      "name": "Ava Chen",
      "profile": "string",
      "street": "string",
      "url": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Companies action reference](actions/lookup-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/implisenseAPI/latest/actions/lookup-companies).
