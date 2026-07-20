# Bulldog-WP: Get session health

Retrieves session health from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/device-health?${params}`, {
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
| `deviceId` | string | yes | WhatsApp number device ID from Bulldog WP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastOnlineAt": "2026-05-07T12:00:00.000Z",
      "lastSyncAt": "2026-05-07T12:00:00.000Z",
      "lastSyncSeconds": 1,
      "ok": true,
      "operative": true,
      "queue": {},
      "status": "string",
      "subscription": "string",
      "synced": true,
      "uptime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastOnlineAt` | date |  |
| `lastSyncAt` | date |  |
| `lastSyncSeconds` | number |  |
| `ok` | boolean |  |
| `operative` | boolean |  |
| `queue` | object |  |
| `status` | string |  |
| `subscription` | string |  |
| `synced` | boolean |  |
| `uptime` | number |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /devices/{deviceId}/health` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/device-health.md) for the provider-specific parameters and requirements.

