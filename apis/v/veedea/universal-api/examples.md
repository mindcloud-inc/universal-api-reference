# Veedea Universal API Examples

These examples use the MindCloud API key and Veedea connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Auth Token

Retrieves an auth token from Veedea.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Token action reference](actions/get-auth-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veedea/latest/actions/get-auth-token).
