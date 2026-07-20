# LightwaveRF Heating: Get Room

Retrieves a room from LightwaveRF Heating.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Heating `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-room?connectionId=$CONNECTION_ID&roomId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-room?${params}`, {
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
| `roomId` | string | yes | The LightwaveRF room identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "devices": [
        {}
      ],
      "features": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `devices` | array<object> | Devices in the room. |
| `features` | array<object> | Features in the room. |
| `id` | string | Room identifier. |
| `name` | string | Room name. |

## Native endpoint

Through the native LightwaveRF Heating API, this operation is `GET /v1/room/{roomId}` (base URL `https://publicapi.lightwaverf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room.md) for the provider-specific parameters and requirements.

