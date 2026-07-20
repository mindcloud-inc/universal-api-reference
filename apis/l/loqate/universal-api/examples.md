# Loqate Universal API Examples

These examples use the MindCloud API key and Loqate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Addresses

Finds addresses in Loqate by search text.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses?connectionId=$CONNECTION_ID&text=Loqate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Loqate"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses?${params}`, {
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
      "description": "string",
      "highlight": "string",
      "id": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Find Addresses action reference](actions/find-addresses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loqate/latest/actions/find-addresses).
