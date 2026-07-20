# Cloudmersive Security Universal API Examples

These examples use the MindCloud API key and Cloudmersive Security connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check IP Bot Status

Checks an IP address for bot threats in Cloudmersive Security.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status?connectionId=$CONNECTION_ID&ipAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ipAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status?${params}`, {
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
      "IsBot": true
    }
  ],
  "meta": {}
}
```

See the full [Check IP Bot Status action reference](actions/check-ip-bot-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersiveSecurity/latest/actions/check-ip-bot-status).
