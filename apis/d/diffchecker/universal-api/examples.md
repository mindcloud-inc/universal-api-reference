# Diffchecker Universal API Examples

These examples use the MindCloud API key and Diffchecker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication

Tests Diffchecker API authentication with the current API key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/test-authentication?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diffchecker/latest/actions/test-authentication).
