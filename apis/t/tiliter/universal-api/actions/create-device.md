# Tiliter: Create Device

Creates a device in the Tiliter Recognition API.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceIdPath": "string",
  "deviceId": "string",
  "cameras[]": [
    "string"
  ],
  "operationalMode": "string",
  "storeId": "string",
  "departments[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceIdPath": "string",
    "deviceId": "string",
    "cameras[]": ["string"],
    "cameras[]": ["string"],
    "operationalMode": "string",
    "storeId": "string",
    "departments[]": ["string"],
    "departments[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceIdPath` | string | yes |  |
| `deviceId` | string | yes | Device ID in the request body. Must match Device ID Path. |
| `cameras[]` | array<string> | yes |  |
| `cameras[]` | array<string> | yes |  |
| `operationalMode` | string | yes |  |
| `storeId` | string | yes |  |
| `departments[]` | array<string> | yes |  |
| `departments[]` | array<string> | yes |  |

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

Through the native Tiliter API, this operation is `POST /devices/:device_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-device.md) for the provider-specific parameters and requirements.

