# Ubidots: Get Device Variable



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-variable?connectionId=$CONNECTION_ID&deviceKey=string&variableKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceKey": "string",
  "variableKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-device-variable?${params}`, {
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
| `deviceKey` | string | yes | The device ID or API label. |
| `variableKey` | string | yes | The variable API label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "device": {},
      "id": "string",
      "label": "string",
      "lastValue": {},
      "name": "Ava Chen",
      "properties": {},
      "tags": [
        "string"
      ],
      "type": "string",
      "unit": "string",
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
| `device` | object |  |
| `id` | string |  |
| `label` | string |  |
| `lastValue` | object |  |
| `name` | string |  |
| `properties` | object |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `unit` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /devices/:device_key/variables/:variable_key/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-variable.md) for the provider-specific parameters and requirements.

