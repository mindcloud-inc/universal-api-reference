# Element: Create Room

Creates a room in Element.

```
POST https://connect.mindcloud.co/v1/universal/element/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/element/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/element/latest/actions/create-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional room name for the new room. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "room_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `room_id` | string |  |

## Native endpoint

Through the native Element API, this operation is `POST /_matrix/client/v3/createRoom` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

