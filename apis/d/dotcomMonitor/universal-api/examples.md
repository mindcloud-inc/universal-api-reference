# Dotcom Monitor Universal API Examples

These examples use the MindCloud API key and Dotcom Monitor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate

Authenticates with Dotcom Monitor and starts a session.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/authenticate?${params}`, {
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

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dotcomMonitor/latest/actions/authenticate).

## Disable Alerts for Device

Disables alerts for a device in Dotcom Monitor temporarily.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/disable-alerts-for-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertSilenceMin": 1,
  "deviceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/disable-alerts-for-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertSilenceMin": 1,
    "deviceId": "string"
  })
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

See the full [Disable Alerts for Device action reference](actions/disable-alerts-for-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dotcomMonitor/latest/actions/disable-alerts-for-device).
