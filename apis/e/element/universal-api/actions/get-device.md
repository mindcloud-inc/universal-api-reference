# Element: Get Device

Retrieves a device from Element.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-device?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/get-device?${params}`, {
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
| `deviceId` | string | yes | Matrix device ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device_id": "string",
      "display_name": "Ava Chen",
      "last_seen_ip": "string",
      "last_seen_ts": 1,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device_id` | string |  |
| `display_name` | string |  |
| `last_seen_ip` | string |  |
| `last_seen_ts` | number |  |
| `user_id` | string |  |

## Native endpoint

Through the native Element API, this operation is `GET /_matrix/client/v3/devices/:deviceId` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

