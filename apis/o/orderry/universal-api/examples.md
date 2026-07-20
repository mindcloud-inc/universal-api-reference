# Orderry Universal API Examples

These examples use the MindCloud API key and Orderry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Settings



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings?${params}`, {
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
      "success": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Settings action reference](actions/get-company-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderry/latest/actions/get-company-settings).
