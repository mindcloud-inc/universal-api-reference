# Bulldog-WP Universal API Examples

These examples use the MindCloud API key and Bulldog-WP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get session health

Retrieves session health from Bulldog-WP.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health?${params}`, {
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
      "lastOnlineAt": "2026-05-07T12:00:00.000Z",
      "lastSyncAt": "2026-05-07T12:00:00.000Z",
      "lastSyncSeconds": 1,
      "ok": true,
      "operative": true,
      "queue": {},
      "status": "string",
      "subscription": "string",
      "synced": true,
      "uptime": 1
    }
  ],
  "meta": {}
}
```

See the full [Get session health action reference](actions/device-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bulldogWP/latest/actions/device-health).
