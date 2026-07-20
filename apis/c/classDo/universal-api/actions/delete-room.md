# ClassDo: Delete Room

Deletes an existing room from ClassDo.

```
DELETE https://connect.mindcloud.co/v1/universal/classDo/latest/actions/delete-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/delete-room?connectionId=$CONNECTION_ID&query=mutation%20DeleteRoom%20%7B%20deleteRoom(id%3A%20%22ROOM_ID%22)%20%7B%20id%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "mutation DeleteRoom { deleteRoom(id: \"ROOM_ID\") { id } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classDo/latest/actions/delete-room?${params}`, {
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
| `query` | string | yes | GraphQL mutation payload. Default: `mutation DeleteRoom { deleteRoom(id: \"ROOM_ID\") { id } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deleteRoom": {
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
| `data.deleteRoom.id` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room.md) for the provider-specific parameters and requirements.

