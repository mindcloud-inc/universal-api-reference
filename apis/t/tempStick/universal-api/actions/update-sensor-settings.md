# Temp Stick: Update Sensor Settings

Updates settings for an existing Temp Stick sensor.

```
PUT https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/update-sensor-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sensorId` | string | yes | Sensor ID |
| `sensorName` | string | yes | The display name for the sensor. |
| `sendInterval` | number | yes | How often the sensor reports readings, in seconds. Default: `300`. |
| `useAlertInterval` | number | yes | Whether alert interval throttling is enabled. Default: `0`. |
| `alertInterval` | number | yes | Minimum time between alert notifications, in minutes. Default: `0`. |
| `alertTempBelow` | number | no | Trigger an alert when temperature falls below this threshold. |
| `alertTempAbove` | number | no | Trigger an alert when temperature rises above this threshold. |
| `alertHumidityBelow` | number | no | Trigger an alert when humidity falls below this threshold. |
| `alertHumidityAbove` | number | no | Trigger an alert when humidity rises above this threshold. |
| `connectionSensitivity` | number | yes | Connection sensitivity setting for the sensor. Default: `1`. |
| `useOffset` | number | yes | Whether temperature and humidity offsets are enabled. Default: `0`. |
| `tempOffset` | number | yes | Temperature offset applied to readings. Default: `0`. |
| `humidityOffset` | number | yes | Humidity offset applied to readings. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `POST /sensor/:sensor_id` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sensor-settings.md) for the provider-specific parameters and requirements.

