# ClassDo: Add Room Members

Adds members to a room in ClassDo.

```
POST https://connect.mindcloud.co/v1/universal/classDo/latest/actions/add-room-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/add-room-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation AddRoomMembers { addRoomMembers(data: { roomId: \"ROOM_ID\", userIds: [\"USER_ID\"] }) { id } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classDo/latest/actions/add-room-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation AddRoomMembers { addRoomMembers(data: { roomId: \"ROOM_ID\", userIds: [\"USER_ID\"] }) { id } }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation payload. Default: `mutation AddRoomMembers { addRoomMembers(data: { roomId: \"ROOM_ID\", userIds: [\"USER_ID\"] }) { id } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "addRoomMembers": {
          "id": "string"
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
| `data.addRoomMembers.id` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-room-members.md) for the provider-specific parameters and requirements.

