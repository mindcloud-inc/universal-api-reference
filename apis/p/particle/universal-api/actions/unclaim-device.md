# Particle: Unclaim Device



```
DELETE https://connect.mindcloud.co/v1/universal/particle/latest/actions/unclaim-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/particle/latest/actions/unclaim-device?connectionId=$CONNECTION_ID&deviceId=0123456789abcdef01234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "0123456789abcdef01234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/unclaim-device?${params}`, {
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
| `deviceId` | string | yes | Default: `0123456789abcdef01234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Particle API, this operation is `DELETE /v1/devices/:deviceId` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unclaim-device.md) for the provider-specific parameters and requirements.

