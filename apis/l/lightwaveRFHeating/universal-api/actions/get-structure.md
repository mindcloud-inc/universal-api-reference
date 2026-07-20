# LightwaveRF Heating: Get Structure

Retrieves a structure from LightwaveRF Heating.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Heating `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-structure?connectionId=$CONNECTION_ID&structureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "structureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-structure?${params}`, {
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
| `structureId` | string | yes | The LightwaveRF structure identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "rooms": [
        {}
      ],
      "zones": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Structure identifier. |
| `name` | string | Structure name. |
| `rooms` | array<object> | Rooms in the structure. |
| `zones` | array<object> | Zones in the structure. |

## Native endpoint

Through the native LightwaveRF Heating API, this operation is `GET /v1/structure/{structureId}` (base URL `https://publicapi.lightwaverf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-structure.md) for the provider-specific parameters and requirements.

