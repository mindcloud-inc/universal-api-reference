# Airzone Cloud: Update Device Parameter

Updates a device parameter in Airzone Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-device-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-device-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "string",
  "installationId": "string",
  "param": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-device-parameter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "string",
    "installationId": "string",
    "param": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | The Airzone device identifier. |
| `installationId` | string | yes | The installation ID that owns the device. |
| `param` | string | yes | The device parameter to change. |
| `value` | string | yes | The new parameter value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opts` | object | no | Optional object for extra settings, such as `units` when updating a setpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the device parameter update request succeeded. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `PATCH /devices/{deviceId}` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-device-parameter.md) for the provider-specific parameters and requirements.

