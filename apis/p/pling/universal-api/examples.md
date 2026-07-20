# Pling Universal API Examples

These examples use the MindCloud API key and Pling connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Configuration

Retrieves OCS API configuration details from Pling.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration?${params}`, {
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
      "contact": "string",
      "host": "string",
      "ssl": true,
      "version": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Configuration action reference](actions/get-api-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pling/latest/actions/get-api-configuration).
