# Supernotes Universal API Examples

These examples use the MindCloud API key and Supernotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Auth

Checks your Supernotes API token and returns the user ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/check-auth?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/check-auth?${params}`, {
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
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Auth action reference](actions/check-auth.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supernotes/latest/actions/check-auth).
