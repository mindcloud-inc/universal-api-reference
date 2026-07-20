# LightwaveRF Power: Update Room

Updates an existing room in LightwaveRF Power.

```
PUT https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | yes | The LightwaveRF room identifier to update. |
| `name` | string | no | The updated room name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "name": "Ava Chen",
      "order": [
        "string"
      ],
      "parentGroups": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `name` | string |  |
| `order` | array<string> |  |
| `parentGroups` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `PUT /v1/room/{roomId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room.md) for the provider-specific parameters and requirements.

