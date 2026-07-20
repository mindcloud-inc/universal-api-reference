# Ordoro Universal API Examples

These examples use the MindCloud API key and Ordoro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Authentication Status

Retrieves the authentication status from Ordoro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/check-authentication-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/check-authentication-status?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Authentication Status action reference](actions/check-authentication-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ordoro/latest/actions/check-authentication-status).
