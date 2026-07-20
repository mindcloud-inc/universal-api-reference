# Tiliter: Get Device

Retrieves a device from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-device?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-device?${params}`, {
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
| `deviceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cameras": [
        "string"
      ],
      "departments": [
        "string"
      ],
      "deviceId": "string",
      "operationalMode": "string",
      "storeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cameras` | array<string> |  |
| `cameras[]` | string |  |
| `departments` | array<string> |  |
| `departments[]` | string |  |
| `deviceId` | string |  |
| `operationalMode` | string |  |
| `storeId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /devices/:device_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

