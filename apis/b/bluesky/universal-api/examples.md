# Bluesky Universal API Examples

These examples use the MindCloud API key and Bluesky connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Session

Retrieves the current Bluesky session details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-session?${params}`, {
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
      "did": "string",
      "didDoc": {},
      "email": "ava@example.com",
      "emailAuthFactor": true,
      "emailConfirmed": true,
      "handle": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Session action reference](actions/get-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bluesky/latest/actions/get-session).
