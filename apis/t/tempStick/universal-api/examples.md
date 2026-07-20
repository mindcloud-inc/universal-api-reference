# Temp Stick Universal API Examples

These examples use the MindCloud API key and Temp Stick connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current Temp Stick user details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-current-user?${params}`, {
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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tempStick/latest/actions/get-current-user).

## Update Sensor Settings

Updates settings for an existing Temp Stick sensor.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-sensor-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sensorId": "string",
  "sensorName": "Ava Chen",
  "sendInterval": "300",
  "useAlertInterval": "0",
  "alertInterval": "0",
  "connectionSensitivity": "1",
  "useOffset": "0",
  "tempOffset": "0",
  "humidityOffset": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-sensor-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sensorId": "string",
    "sensorName": "Ava Chen",
    "sendInterval": "300",
    "useAlertInterval": "0",
    "alertInterval": "0",
    "connectionSensitivity": "1",
    "useOffset": "0",
    "tempOffset": "0",
    "humidityOffset": "0"
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

See the full [Update Sensor Settings action reference](actions/update-sensor-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tempStick/latest/actions/update-sensor-settings).
