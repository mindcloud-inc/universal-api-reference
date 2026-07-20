# Dotcom Monitor: Disable Alerts for Device

Disables alerts for a device in Dotcom Monitor temporarily.

```
PUT https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/disable-alerts-for-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotcom Monitor `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alertSilenceMin` | number | yes | The number of minutes to disable alerts for this device. |
| `deviceId` | string | yes | The unique monitoring device ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotcom Monitor API returns.

## Native endpoint

Through the native Dotcom Monitor API, this operation is `POST /device/:deviceId/DisableAlert` (base URL `https://api.dotcom-monitor.com/config_api_v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-alerts-for-device.md) for the provider-specific parameters and requirements.

