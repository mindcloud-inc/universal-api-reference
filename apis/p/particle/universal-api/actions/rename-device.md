# Particle: Rename Device



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/rename-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/rename-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "0123456789abcdef01234567",
  "name": "mindcloud-device"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/rename-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "0123456789abcdef01234567",
    "name": "mindcloud-device"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | Default: `0123456789abcdef01234567`. |
| `name` | string | yes | Default: `mindcloud-device`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connected": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connected` | boolean |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Particle API, this operation is `PUT /v1/devices/:deviceId` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-device.md) for the provider-specific parameters and requirements.

