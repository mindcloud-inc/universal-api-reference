# 2Smart Cloud: Check if there is biometric keys for this device



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-devices-by-device-id-check-biometric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-devices-by-device-id-check-biometric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-devices-by-device-id-check-biometric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device_id` | string | yes | Device ID in broker |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /devices/{device_id}/check-biometric` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-devices-by-device-id-check-biometric.md) for the provider-specific parameters and requirements.

