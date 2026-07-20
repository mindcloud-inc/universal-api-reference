# ClassDo: Create Room

Creates a new room in ClassDo.

```
POST https://connect.mindcloud.co/v1/universal/classDo/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CreateRoom { createRoom(data: { name: \"New Room\", description: \"Created from MindCloud\" }) { id name } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classDo/latest/actions/create-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CreateRoom { createRoom(data: { name: \"New Room\", description: \"Created from MindCloud\" }) { id name } }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation payload. Default: `mutation CreateRoom { createRoom(data: { name: \"New Room\", description: \"Created from MindCloud\" }) { id name } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createRoom": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createRoom.id` | string |  |
| `data.createRoom.name` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

