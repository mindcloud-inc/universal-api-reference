# Socket: Get Telemetry Config

Retrieves an organization telemetry configuration from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-telemetry-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-telemetry-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-telemetry-config?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Socket API, this operation is `GET /orgs/:org_slug/telemetry/config` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-telemetry-config.md) for the provider-specific parameters and requirements.

