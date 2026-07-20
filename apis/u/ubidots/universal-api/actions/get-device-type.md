# Ubidots: Get Device Type



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-type?connectionId=$CONNECTION_ID&deviceTypeKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceTypeKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-type?${params}`, {
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
| `deviceTypeKey` | string | yes | The device type ID or key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "devicesUrl": "https://example.com",
      "id": "string",
      "label": "string",
      "name": "Ava Chen",
      "properties": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `devicesUrl` | string |  |
| `id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `properties` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /device_types/:device_type_key/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-type.md) for the provider-specific parameters and requirements.

