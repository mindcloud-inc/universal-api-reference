# GSA Site Scanning Universal API Examples

These examples use the MindCloud API key and GSA Site Scanning connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Scan Device

Retrieves a scan device by device ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device?connectionId=$CONNECTION_ID&deviceId=scanner-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "scanner-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device?${params}`, {
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
      "deviceId": "string",
      "deviceInUse": true,
      "deviceStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Scan Device action reference](actions/get-scan-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gSASiteScanning/latest/actions/get-scan-device).

## Start Scanning

Requests a scan device to start sending scan data.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/start-scanning" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/start-scanning', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "00000000-0000-0000-0000-000000000000"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accessExpiryTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Start Scanning action reference](actions/start-scanning.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gSASiteScanning/latest/actions/start-scanning).
