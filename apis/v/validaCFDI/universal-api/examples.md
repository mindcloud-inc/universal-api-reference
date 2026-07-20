# ValidaCFDI Universal API Examples

These examples use the MindCloud API key and ValidaCFDI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Connection

Tests the API connection in ValidaCFDI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection?${params}`, {
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
      "authenticated": true,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "message": "string",
      "planTier": "string",
      "userId": 1,
      "validationsRemaining": 1
    }
  ],
  "meta": {}
}
```

See the full [Test API Connection action reference](actions/test-api-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/validaCFDI/latest/actions/test-api-connection).
