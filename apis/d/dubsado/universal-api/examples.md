# Dubsado Universal API Examples

These examples use the MindCloud API key and Dubsado connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Zapier API Key

Validates a Zapier API key in Dubsado.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key?${params}`, {
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
      "brand": "string",
      "code": "string",
      "description": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Zapier API Key action reference](actions/validate-zapier-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dubsado/latest/actions/validate-zapier-api-key).
