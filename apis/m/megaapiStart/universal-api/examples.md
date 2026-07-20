# Megaapi Start Universal API Examples

These examples use the MindCloud API key and Megaapi Start connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Connection Status

Retrieves WhatsApp connection status from Megaapi Start.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Connection Status action reference](actions/get-connection-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/megaapiStart/latest/actions/get-connection-status).
