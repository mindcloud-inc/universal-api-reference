# Airzone Cloud: Get Device Status

Retrieves a device's state from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-device-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-device-status?connectionId=$CONNECTION_ID&deviceId=string&installationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string",
  "installationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-device-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | The Airzone device identifier. |
| `installationId` | string | yes | The installation ID that owns the device. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "isConnected": true,
      "name": "Ava Chen",
      "power": true,
      "warnings": [
        {}
      ],
      "ws_connected": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Device errors. |
| `isConnected` | boolean | Whether the device is reachable. |
| `name` | string | Device name when available. |
| `power` | boolean | Current power state when applicable. |
| `warnings` | array<object> | Device warnings. |
| `ws_connected` | boolean | Whether the webserver is reachable. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /devices/{deviceId}/status` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-status.md) for the provider-specific parameters and requirements.

