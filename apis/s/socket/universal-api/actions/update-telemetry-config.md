# Socket: Update Telemetry Config

Updates an organization telemetry configuration in Socket.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-telemetry-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-telemetry-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-telemetry-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "telemetry": {
        "enabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `telemetry` | object | Telemetry configuration |
| `telemetry.enabled` | boolean | Telemetry enabled |

## Native endpoint

Through the native Socket API, this operation is `PUT /orgs/:org_slug/telemetry/config` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-telemetry-config.md) for the provider-specific parameters and requirements.

