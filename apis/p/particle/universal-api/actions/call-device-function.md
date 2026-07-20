# Particle: Call Device Function



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/call-device-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/call-device-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arg": "test",
  "deviceId": "0123456789abcdef01234567",
  "functionName": "testFunction"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/call-device-function', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arg": "test",
    "deviceId": "0123456789abcdef01234567",
    "functionName": "testFunction"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arg` | string | yes | Default: `test`. |
| `deviceId` | string | yes | Default: `0123456789abcdef01234567`. |
| `functionName` | string | yes | Default: `testFunction`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connected": true,
      "id": "string",
      "returnValue": 1
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
| `returnValue` | number |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/devices/:deviceId/:functionName` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-device-function.md) for the provider-specific parameters and requirements.

